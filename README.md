# Style Guide WIP Readme

## Notes to self

**TO DO:** 
* add `liquify` syntax to `_include` files
    * also, figure out how to add Liquid variables to data files; do I need to define the variables in the page where the content is output (i.e., the collection page)? or can I use a global variable of some sort (site.url type stuff) directly in the YAML file without having to define its value elsewhere?
* write up implementation of `liquify` for this readme 
* set up sidebar nav
* add the rest of the style rules
* rule formatting (both in CSS and YAML files themselves)
* "featured" rules + minimum threshold rules

## Repo basics

All of the following information relates to the `main` branch. For all intents and purposes, ignore (but do not delete) the `gh-pages` branch. Everything is configured as intended. (For more information, see the `.github/workflows/build-jekyll.yml` section below.)

### `_data/stylerules`

The actual style rules are hosted here (in the form of YAML files). If the Liquify plugin is enabled, you can use Liquid tags in the actual data files and "liquify" them later.

### `_includes`

The Liquid tags that pull style rules from their data files. Designed to be modular so you can include the file (`get_all_rules.md` to get all rules or `get_rules_for_audience` to get rules for a specific audience) in your output page rather than re-typing the Liquid all over again.
    
#### `get_all_rules.md`
Outputs every single rule in a given `_data/stylerules/` file. 
    
**Usage** (when including in an actual page):
``` 
{% assign file = site.data.stylerules.[YOURFILE] %}

{% include get_all_rules.md filename=file %}
```

#### `get_rules_for_audience`
Outputs every applicable rule in a given `_data/stylerules/` file based on your audience of choice (current options: `dev`, `marketing`, and `techdocs`). 

> **NOTE** : Does not accept `all` as an audience. If you want to output all style rules, use `get_all_rules.md` instead.

**Usage** (when including in an actual page):
```
{% assign file = site.data.stylerules.[YOURFILE] %}
{% assign aud = "[YOURAUDIENCE]" %}

{% include get_rules_for_audience.md filename=file audience=aud %}
```             
### `_plugins/liquify.rb`

Sourced from [here](https://github.com/vividh/liquify). For more information about using Liquify, see below. 

> **NOTE:** If you add any additional plugins, make sure to update the Gemfile as well!

### `_github/workflows/build-jekyll.yml`

A custom GitHub Actions workflow that lets you deploy the GitHub Pages site as if you were running Jekyll locally (even though I'm currently not). Crucial if I want to use non-approved plugins like Liquify. Some details:

* The GitHub Pages branch must be set to `gh-pages` rather than `main`. 

* Every time you push a change to `main`, the `build-jekyll` workflow will automatically crate the "actual" site files and push them to `gh-pages`.

* GitHub's default GitHub Action will then automatically generate the GitHub pages site from the `gh-pages` repo.

In other words, stick to making changes in `main` as usual and don't touch anything in `gh-pages`. 

### `audiences`

The collections folder for the actual style guide output. Each audience has its own subfolder (`audiences/_all`, `audiences/_dev`, `audiences/_marketing`, and `audiences/_techdocs`), and each subfolder contains the pages associated with that audiences.

* For example, `audiences/_dev/grammar.md` generates a page you can visit at https://alexakreizinger.github.io/styleguide/marketing/grammar/. 

* The page itself pulls data from `_data/stylerules/grammar.yml`. It does this by using `include` to call upon the `get_rules_for_audience.md` (where the filename is `site.data.stylerules.grammar` and the audience is `dev`).

* As such, the output will include all style rules from `_data/stylerules/grammar.yml` that are aimed at developers.

> **NOTE:** New subfolders must be added to the `collections` item in `_config.yml`. Subfolders must start with an underscore (`audiences/_marketing`), but their entry in `_config.yml` must not (`marketing`).

### `pages`

Any pages that don't fall under `audiences`. 

### `YAMLtemplate.yml`

Template for the YAML files in `_data/stylerules`.

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

* Your theme (at least with the Minima theme, haven't tried any others yet) will break unless your `_config.yml` file includes `url: https://alexakreizinger.github.io` and `baseurl: /styleguide`.

* The custom GitHub Action that lets you use plugins that haven't been approved by GitHub Pages (*without* running Jekyll locally) won't work unless you include `target_branch: 'gh-pages'` in the last line of the file in `.github/workflows/build-jekyll.yml`.

* Collection files need YAML frontmatter or their pages won't render. This was a major point of confusion for a while because the official Jekyll documentation said they *wouldn't* need frontmatter... but apparently the Jekyll documentation lies.

* To get multiline bullet points for `examples`, either use a <br> tag after the first line or use two spaces after the first line, like so:

```
This will be rendered as a multi-line bullet point.<br>
It has two lines!
```

```
This will be rendered as a multi-line bullet point.  #there are two spaces here
It has two lines!
```