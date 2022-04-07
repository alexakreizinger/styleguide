# Style Guide WIP Readme

## Repo basics

All of the following information relates to the `main` branch. For all intents and purposes, ignore (but do not delete) the `gh-pages` branch. Everything is configured as intended. (For more information, see the `.github/workflows/build-jekyll.yml` section below.)

### `_data/stylerules`

The actual style rules are hosted here (in the form of YAML files). If the Liquify plugin is enabled, you can use Liquid tags in the actual data files and "liquify" them later.

### `_includes`

The Liquid tags that pull style rules from their data files. Designed to be modular so you can include the file in your output page rather than re-typing the Liquid all over again.

#### `get_all_rules.md`
Outputs every single rule in a given `_data/stylerules/` file. Currently used for the semi-secret `/all/` pages.
    
**Usage** (when including in an actual page):
``` 
{% assign file = site.data.stylerules.[YOURFILE] %}

{% include get_all_rules.md filename=file %}
```

#### `get_rules_for_audience`
Outputs every applicable rule in a given `_data/stylerules/` file based on your audience of choice (current options: `dev`, `mktg`, and `tw`). 

> **NOTE** : Does not accept `all` as an audience. If you want to output all style rules, use `get_all_rules.md` instead.

**Usage** (when including in an actual page):
```
{% assign file = site.data.stylerules.[YOURFILE] %}
{% assign aud = "[YOURAUDIENCE]" %}

{% include get_rules_for_audience.md filename=file audience=aud %}
```             
#### `get_featured_rules_for_audience`
Outputs every "featured" rule in a given `_data/stylerules/` file based on your audience of choice (current options: `dev`, `mktg`, and `tw`). Currently used on parent pages for each audience.

**Usage** (when including in an actual page):
```
{% assign aud = "[YOURAUDIENCE]" %}
{% assign file1 = site.data.stylerules.[YOURFILE] %}
{% assign section1 = "[SECTIONNAME]" %}
{% capture link1 %}{{site.baseurl}}{{page.permalink}}[URL-OF-PAGE-WHERE-THESE-RULES-APPEAR/]{% endcapture %}

{% include get_featured_rules_for_audience.md filename=file1 audience=aud sectionname=section1 sectionlink=link1 %}
```
> **NOTE** : You'll need to repeat `file1`/`section1`/`link1` (and its associated `include` statement) as many times as needed to fetch the features rules from every section. However, `aud` should be consistent, so there's no need to repeat that part.

### `_plugins/liquify.rb`

Sourced from [here](https://github.com/vividh/liquify). For more information about using Liquify, see below. 

> **NOTE:** If you add any additional plugins, make sure to update the Gemfile as well!

### `_github/workflows/build-jekyll.yml`

A custom GitHub Actions workflow that lets you deploy the GitHub Pages site as if you were running Jekyll locally (even though I'm currently not). Crucial if I want to use non-approved plugins like Liquify. Some details:

* The GitHub Pages branch must be set to `gh-pages` rather than `main`. 

* Every time you push a change to `main`, the `build-jekyll` workflow will automatically crate the "actual" site files and push them to `gh-pages`.

* GitHub's default GitHub Action will then automatically generate the GitHub pages site from the `gh-pages` repo.

In other words, stick to making changes in `main` as usual and don't touch anything in `gh-pages`. 

### `pages`

The `pages` folder for the actual style guide output. Each audience has its own subfolder (`pages/dev`, `pages/mktg`, and `pages/tw`), and each subfolder contains the pages associated with that audience.

> **NOTE:** The `^[AUDIENCE].index.md` files start with a caret so that the index file will appear first alphabetically (because it's convenient when it's at the top of the list). The caret doesn't serve an actual purpose, Jekyll-wise.

* For example, `pages/mktg/grammar.md` generates a page you can visit at https://alexakreizinger.github.io/styleguide/mktg/grammar/. 

* The page itself pulls data from `_data/stylerules/grammar.yml`. It does this by using `include` to call upon the `get_rules_for_audience.md` (where the filename is `site.data.stylerules.grammar` and the audience is `dev`).

* As such, the output will include all style rules from `_data/stylerules/grammar.yml` that are aimed at developers.

#### **All**
* audience: all
* url: `all`
* title: All
* (semi-secret; hidden from nav and search)
#### **Developers**
* audience: `dev`
* url: `/dev/`
* title: Developers
#### **Marketers**: 
* audience: `mktg`
* url: `/mktg/`
* title: Marketers
#### **Technical Writers**
* audience: `tw`
* url: `/tw/`
* title: Technical Writers

> **NOTE:** Turns out that some of the Liquid stuff for autogenerating links between pages is way easier when an audience's `audience` value and `url` slug are the same. (The `all` audience now has an audience key just to make the URL part easier, even though the audience value isn't used to fetch any rules from the YAML files.)

### `YAMLtemplate.yml`

Template for the YAML files in `_data/stylerules`. Not actually referenced by any other pages, this is just a regular old template.

## Using Liquify

If output from a `{{ Liquid tag }}`' includes text that *itself* contains a Liquid tag, you can use the `{{ content | liquify }}` syntax to also parse the output's own Liquid tags and populate them accordingly.

For example:

`page.md` contains the following front matter and content:

```
---
title: My Page
tagline: {{ page.title }} — Population: You
---

{{ page.tagline }}
```
Under normal circumstances, this would render the following output (the literal contents of the `page.tagline` item):

`{{ page.title }} — Population: You`

However, if you use `liquify` in `page.md`...
```
---
title: My Page
tagline: {{ page.title }} — Population: You
---

{{ page.tagline | liquify }}
```
...you'd render the following output (with the `page.tagline` item's own Liquid rendered accordingly):

`My Page - Population: You`

> **NOTE:** Tags are parsed on the final page or file they're rendered on, not the page or file in which `liquify` is initially called. That is to say, if you use `include` to call upon another page that uses the `liquify` tag, the tag will use any `page.variables` from the page where the `include` was *called*, not the location of the include file itself. 
>
> To see this in action, consult `pages/testpage.md`, which calls upon `_includes/testinclude.md` to pull data from `_data/test.yml`.

(WRITE UP EXPLANATION OF HOW I ACTUALLY IMPLEMENT THIS W/ RELATIVE URLS IN THE STYLE GUIDE YAML FILES OR WHATEVER)

## Things I don't fully understand but will probably come up later so I'm writing them down now

* Your theme will break unless your `_config.yml` file includes `url: https://alexakreizinger.github.io` and `baseurl: /styleguide`.

* The custom GitHub Action that lets you use plugins that haven't been approved by GitHub Pages (*without* running Jekyll locally) won't work unless you include `target_branch: 'gh-pages'` in the last line of the file in `.github/workflows/build-jekyll.yml`.

* Collection files need YAML frontmatter or their pages won't render. This was a major point of confusion for a while because the official Jekyll documentation said they *wouldn't* need frontmatter... but apparently the Jekyll documentation lies.

* To get multiline bullet points for `rules` or `examples`, either use a <br> tag after the first line or use two spaces after the first line, like so:

```
This will be rendered as a multi-line bullet point.<br>
It has two lines!
```

```
This will be rendered as a multi-line bullet point.  #there are two spaces here
It has two lines!
```

> **NOTE:** I don't include the actual bullet points in these examples because the bullet point itself is rendered by the `get_all_rules` and `get_rules_For_audience` files, not in the YAML file where the data is actually written/stored. You need to use the <br> or two spaces in the YAML file, not in the include files.

* Plugins suddenly not working? Make sure you don't have `github-pages` anywhere in your Gemfile or `_config.yml`—this will disable custom plugins from loading unless you remove it.

* If you're having issues getting images from the `assets` folder to display properly, try using the `{{ site.url }}{{ site.baseurl }}/assets/images/cats.png` path.

* If you're using the Just the Docs theme and want your sidebar nav to have unclickable parent pages, just make the parent URL and the first child's URL equal the same path—for example, both `^_mktg_index.md` and `mktg_grammar.md` would have a path of `/mktg/grammar/`. However, all other parent/child requirements must be implemented as normal.
