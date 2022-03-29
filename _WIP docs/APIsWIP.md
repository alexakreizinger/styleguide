## Best practices

### Be descriptive and thorough<br>
Make sure your documentation is a comprehensive reference that includes every piece of information your reader needs to know. Don't assume that your reader knows the usage, definition, or implementation of any part of your API or SDK!

### Describe (almost) everything<br>
Include a description for almost every aspect of your API or SDK, including (but not limited to) every class, constant, field, and method. Methods in particular should include a description of each parameter, return value, and possible exceptions thrown.

### Code elements as plural nouns<br>
Don't use elements of your code (like the names of classes or parameters) as plural nouns.
**No:** Use `coolBlocks` to store data.
**Yes:** Use `coolBlock` objects to store data.

### Code elements as verbs<br>
Don't use elements of your code (like the names of methods) as verbs.
**No:** `end()` the program.
**Yes:** Call `end()` to terminate the program.

## Classes

### Introduce classes...<br>
The first sentence of every class description should explain the purpose of that class. 

However, don't just restate the name of the class—in fact, it's better not to include the name of the class at all in the first sentence of your description.

Additionally, don't start your description with phrases like *This class...*; instead, just start explaining what the class is for. This means your first sentence may technically be a sentence fragment (and that's okay).
**Example:**<br>
`Dog`<br>
An animal that can sit, fetch, roll over, and play dead.

### ...then add the rest
The rest of your description (after that first sentence) should include additional information about how and when to use the class, recommended uses, warnings, and so on.

## Constants and fields

### Describe and link<br>
For each constant or field, write a brief description that links back to any relevant methods.

## Methods

### Introduce methods...<br>
The first sentence of every method description should explain what the method does or the action it performs. 

However, don't just restate the name of the method—try to avoid using the name of the method in the first sentence of your description.

Additionally, don't start your description with phrases like *This method...*; instead, just start explaining what the method does. This means your first sentence may technically be a sentence fragment (and that's okay).
**Example:**<br>
`feedDog( Dog dog_name )`<br>
Sends three scoops of kibble to the `Dog` of your choice.

### ...then add the rest
The rest of your description (after that first sentence) should include additional information about how and when to use the method, requirements and prerequisites, exceptions that may occur, and so on.

### Use present tense<br>
Use present tense for method descriptions. For example, you might say that a method  *fetches* data; don't say that it *fetched* or *will fetch* data.

## Text formatting

### Code font<br>
Use `code` font for classes, objects, methods, and so on; however, don't use `code` font for the actual words *class*, *object*, or *method*.

Use `code` font for string literals, but enclose the string in double quotation marks.
**Example:** `"false"`
**Example:** `"Genius of Love"`

### Italics<br>
Use italics for the names of parameters.
**Example:** The `sendBirthdayCard( int Age, String Recipient )` method accepts the parameters *Age* and *Recipient*.