## Callout boxes

### Callout types<br>
Callout boxes let you highlight important information or notices. There are three main types of callout boxes, usually differentiated by their label and color.
(format as examples)
**Info/Note:** A useful (but not urgent) message. Notes often provide clarifying information, tips and tricks, or additional advice.
**Caution/Careful:** An important, semi-urgent message. Caution notes often invite the reader to slow down or tread carefully.
**Warning/Danger:** A critical, urgent message. Wargent notes often contain information that will lead to a serious error if not followed; readers must heed this message at all costs.
[tw, dev]

### Callout frequency<br>
Don't use an excessive number of callout boxes in a single document, and try not to use two callout boxes consecutively with no intervening text between them (if you can avoid it).
[tw, dev]

### Keep callouts short<br>
Try not to use callout boxes that contain long walls of text.
[tw, dev]

## Code samples

### Code formatting<br>
Use `code` font for inline code samples, including method names and variable names.
**Example:** The `isRaining` Boolean can be true or false.
[tw, dev]

### Introduce code samples<br>
Most code samples need an introductory sentence (or paragraph) before the code sample begins. This introduction can end with a period or with a colon.
**Example:**
The following sample shows how to activate your death ray.
` evilLair.deathRay(max_strength); `
[tw, dev]

### Line wrapping<br>
Use line wrapping in long code blocks.
[tw, dev]

## Headings and titles

### Abbreviations in headings and titles<br>
It's okay to use abbreviations in headings and titles as long as you spell out the abbreviation in the subsequent paragraph.

For more information, see [Spell out abbreviations]({{site.baseurl}}{{page.permalink}}grammar/spell-out-abbreviations).
[tw, dev, mktg]

### Include descriptions after every heading<br>
In any kind of public-facing documentation, two headings should never "touch"—every section of a doc needs an introduction, so every heading should be followed by some kind of summary or description before the next subheading appears. Try to provide necessary context for your reader: what is this section describing? Why is it important?

**Example:**
\#\# Mammals
Mammals are warm-blooded animals. They can live in water or on land.
\#\#\# Aquatic mammals
Aquatic mammals are mammals that live primarily or entirely in water, including whales, dolphins, seals, and manatees. However, like all mammals, they still breathe air and must surface periodically to do so.
[tw, dev, mktg]
featured: All subheadings should be followed by a summary or description.

### Heading hierarchy<br>
Don't jump between heading levels. For example, an `h2` heading should not be immediately followed by an `h4` heading.
[tw, dev, mktg]

### Tasks in headings and titles<br>
If a heading or title describes a task, use an infinitive (a "plain" verb) instead of a gerundive (an *-ing* verb).
**No:** Installing Java
**Yes:** Install Java
[tw, dev]

## Images and screenshots

### Captions<br>
Put captions and descriptions after their associated image, not before.
[tw, dev, mktg]

If you're including an image in procedural instructions, this means the image should appear first and its associated step (or steps) should appear afterwards.
[tw, dev]

### When to include screenshots<br>
Screenshots are great, but not always necessary. 

It can be helpful to include a screenshot when you're describing how to navigate a user interface (or are describing the features of an interface), especially if the interface is too complicated to explain with words alone. However, don't include a screenshot in situations that don't need a visual aid.

This also means that some procedural instructions may include screenshots, but not for every step. A single screenshot will often correspond to multiple steps.
[tw, dev]

## Links (MAKE SURE MKTG IS INCLUDED!!!)

### Helpful hyperlinks<br>
In-text hyperlinks are a useful way to direct readers' attention towards similar topics and related materials, especially if you don't want to break the flow of the document to explain an important word or concept. 

Whenever you need to provide additional context for your readers, try linking to another post about that topic, a glossary entry that expands upon the definition of a term, or a guide with more detailed information about a specific parameter or object.
[tw, dev, mktg]

### Descriptive link text<br>
Use descriptive, non-obtrusive link text that doesn't disrupt the flow of the sentence.

For example, for a link to a doc called "Get Started With FraudSensor":
**No:** To get started with FraudSensor (<u>link</u>), you'll need to set up a detection tag.
**Also no:** To get started with Fraudsensor, you'll need to set up a detection tag. <u>Click here to learn more.</u>
**Yes:** To <u>get started with FraudSensor</u>, you'll need to set up a detection tag.

One way to write descriptive links is to use link text that's similar to the title of the link destination or provides additional information about the page you're linking to.

If you include the exact title of a page, match the capitalization of that title. 
**Example:** Follow the steps outlined in <u>Getting Started With FraudSensor</u> before proceeding. 

If you don't include the exact title of a page, capitalize the link text as if it were part of a normal sentence.
**Example:** Make sure you've <u>installed FraudSensor</u> before proceeding.

However, if it's too hard to seamlessly integrate a link into a sentence, you can also write a new, complete sentence that directs readers towards a relevant topic. These sentences should typically begin with a phrase like "For more information," or "To learn more about [topic]," before including the link.
**Example:** For more information, consult our <u>FraudSensor Parameters</u> guide.

### Link the first instance<br>
If you'd like to link to another page that explains a specific term or concept, insert the hyperlink the first time that term or concept appears in the body of the doc (not counting titles or headings).
**Example:** The <u>MediaGuard</u> Dashboard includes data about IVT. Based on this MediaGuard data...
[tw, dev, mktg]


## Lists

### Introduce lists<br>
Most lists need an introductory sentence (or paragraph) before the first list item begins. This introduction can end with a period or with a colon.
[tw, dev, mktg]

### Ordered and unordered lists<br>
When the order of list items isn't important, use a bulleted (unordered) list.
**Example:**<br>
A bicycle has three main components:<br>
* Seat
* Handlebars
* Tires
[tw, dev, mktg]

When the order of list items is important, use a numbered (ordered) list. This usually appplies to sequences of steps or instructions. 
**Example:**
To bake a cake, follow these steps:<br>
1. Mix the batter.
2. Bake in the oven.
3. Decorate to perfection.
[tw, dev, mktg]

However, if a procedure only has one step, use a bulleted (unordered) list instead.
**Example:**<br>
To turn on the light:
* Flip the light switch to the ON position.
[tw, dev]

When presenting a list of options to choose from, use a lettered (ordered) list.
**Example:**<br>
You can choose one of the following colors:<br>
A. Red
B. Yellow
C: Green
[tw, dev, mktg]

### Paired data<br>
For lists that include two pieces of data per list item (like a glossary term and its definition), use a bulleted (unordered) list. 

Format the first piece of data in **bold**, then use a colon to introduce the next piece of data.

**Example:**
The theme park offers three attractions.
* **Screamin' Mean Crazy Coaster:** A high-speed roller coaster. Not recommended for children.
* **Big Joe's River Adventure:** A log ride with water features. Suitable for all ages, but riders will get wet.
* **Schubert Express:** An interactive train tour. Perfect for young guests.
[tw, dev, mktg]

### Parallel structure<br>
Use parallel structure between items in the same list whenever possible. For example, you might start each list item with a verb or write each list item as a complete sentence.
[tw, dev, mktg]

### Sentence case for list items<br>
Use sentence case for list items (including single-word items) unless the list item is case-sensitive or includes a `code` snippet.
[tw, dev, mktg]

### To list or not to list?<br>
If a list has fewer than three items, you might want to present the information in another format instead. 
[tw, dev, mktg]

## Numbers

### When to spell out numbers<br>
Spell out numbers zero through nine when they appear in a sentence, unless a numeral would be more appropriate (like for a version number, file size, or percentage).
**Example:** A bass guitar can have four, five, or six strings.
**Example:** Files should not exceed 8 MB in size.
[tw, dev, mktg]

However, if another numeral appears in the same sentence, use numerals consistently throughout.
**Example:** Of the dentists surveyed, only 1 in 100 recommended using chocolate frosting instead of toothpaste.
[tw, dev, mktg]

Use numerals for numbers 10 and higher.
**Example:** There were 14 penguins at the zoo.
[tw, dev, mktg]

If an ordinal number appears in a sentence (like *first*, *third*, or *twenty-ninth*), spell it out.
**Example:** The seventh page contains information about your warranty.
[tw, dev, mktg]

Spell out indefinite and nonspecific numbers.
**Example:** Millions of people suffer from seasonal allergies.
[tw, dev, mktg]

## Procedures and instructions

### Imperative verbs<br>
When possible, begin each step with an imperative verb. If a dependent clause precedes an independent clause, it's okay if the imperative verb isn't the first word in the sentence.
**Example:** Save your work before continuing.
**Example:** Choose any sword from the display case.
**Example:** To keep the park clean, pick up your trash when you leave.
[tw, dev]

### Introduce procedures<br>
Most procedural instructions need an introductory sentence (or paragraph) before the instructions begin. This introduction can end with a period or with a colon.
[tw, dev]

### List all the steps<br>
Use a numbered list to write out each step in a procedure. However, if a procedure only has one step, use a bulleted list instead.<br>

For more information, see (Ordered and unordered lists)[{{site.baseurl}}{{page.permalink}}formatting-and-organization/#ordered-and-unordered-lists].
[tw, dev]

### Location<br>
If a step requires the reader to perform an action from a specific page, menu, or location, state the location before you describe the action.
**Example:** Using the **Country** drop-down menu, select the country you currently live in.
[tw, dev]

### One action per step<br>
Generally speaking, each step in a procedure should describe a single action.

However, sometimes it's helpful to combine several fast, closely related actions into a single step, especially to describe UI navigation. You can use angle brackets to describe the process of navigating multiple menu items in a row.
**Example:** Select **Filter > Distort > Liquify**.
[tw, dev]

### Outcomes first<br>
If a step includes its intended outcome or goal, describe the outcome of the step before you describe the instructions to carry it out. (In other words, the dependent clause comes first.)
**No:** Select **New file** to create a new file.
**Yes:** To create a new file, select **New file**.
[tw, dev]

### Parallel structure<br>
Try to use parallel structure between different steps in the same procedure.
**Example:**
1. Open the door.
2. Put on your shoes.
3. Grab your keys.
4. Close and lock the door behind you.
[tw, dev]


## Tables

### Introduce tables<br>
Most tables need an introductory sentence (or paragraph) before the table begins. This introduction can end with a period or with a colon.
[tw, dev, mktg]

### Table or list?<br>
If a table only has two columns, you should probably format the information as a [list]({{site.baseurl}}{{page.permalink}}formatting-and-organization/#paired-data) instead.
[tw, dev, mktg]

## Miscellaneous

### Spaces
Use one space after a period (or question mark or exclamation mark), not two.
[tw, dev, mktg]