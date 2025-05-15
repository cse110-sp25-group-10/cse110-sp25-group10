# Team 10x Styling Guidelines
## Table of Contents
### [HTML](#html-styling)
- [Doctype](#Doctype)
- [Document Language](#Document-Language)
- [Charset](#Document-Character-Set)
- [Viewport](#Viewport-Meta-Tag)
- [Validation](#HTML-Validation)
- [Separation of Concerns](#Separation-of-Concerns)
- [Attributes](#Attributes)
  - [Boolean Attributes](#Boolean-Attributes)
- [Case Conventions](#Case-Conventions)
- [Singleton Tags](#Singleton-Tags)
- [Class and ID names](#Class-and-ID-names)
- [Media](#Media)
### [CSS](#css-styling)
- [Structuring](#css-structuring)
- [Validation](#css-validation)
- [!important](#!important)
- [CSS Comments](#css-comments)
- [Declaration Stops](#Declaration-Stops)
- [Property Name Stops](Property-Name-Stops)
- [Rule Separation](#Rule-Separation)
- [Double Quotes around values](#Double-Quotes-around-values)
- [Shorthand vs Longhand](#Shorthand-vs-Longhand)
- [Selectors](#Selectors)
  - [ID Selectors](#ID-Selectors)
  - [Type Selectors](#Type-Selectors)
- [Units](#units)
  - [Relative vs Absolute Units](#Relative-vs-Absolute-Units)
  - [Values to turn off properties](#Values-to-turn-off-properties)
- [Declaration Order](#Declaration-Order)
### [JavaScript](#javascript-styling)
- [Variables](#variables)
  - [Variable Names](#variable-names)
  - [Variable Declaration](#variable-declarations)
- [Strings](#strings)
  - [Template Literals](#template-literals)
- [Operators](#operators)
- [Objects](#objects)
- [Functions](#functions)
- [Loops](#loops)
- [Comments](#comments)

## HTML Styling
### Doctype
Use HTML5. 
```html
<!doctype html>
```
### Document Language
Always set the language using the `lang` tag on the `html` tag.
```html
<html lang="en-US"></html>
```
### Document Character Set
Always set the document character set.
```html
<meta charset="utf-8"></html>
```
### Viewport Meta Tag
Use the viewport meta tag for better use on mobile devices
```html
<meta name="viewport" content="width=device-width">
```
### HTML Validation
Make sure your HTML passes validation before pushing. Use [W3C HTML validator](https://validator.w3.org/nu/)

### Separation of Concerns
Avoid using the style attribute and ```style``` and ```script``` tags whenever possible. Move everything into separate stylesheets/scripts but try to keep as few stylesheets/scripts as possible.
```html
<!-- Avoid -->
<p style="font-size: 1rem">Lorem ipsum.</p>
<script>
  const p = document.querySelector("p");
</script>
```

### Attributes
Use double quotes for attribute values whenever possible
```html
<img src="images/logo.jpg" alt="A circular globe icon" class="no-border">
```
### Boolean Attributes
Leave boolean attributes as is.
```html
<input required>
```

### Case Conventions
Use lowercase for all case-insensitive constructs.
```html
<p class="nice">This looks nice and neat</p>
```
### Singleton Tags
Don't use XHTML styling for singleton tags. *Don't:*
```html
<!-- Don't do this! -->
<input />
```

### Class and ID names
Use semantic class/ID names, and separate multiple words with hyphens (kebab case). Don't use camel case.
```html
<p class="editorial-summary">Blah blah blah</p>
```
### Media
Provide alternative contents for media such as alternative text when possible.
```html
<img src="spreadsheet.png" alt="Spreadsheet screenshot.">
```

## CSS Styling
### CSS Structuring
Use `/* || */` to separate CSS sections for organization so it is easy to navigate to sections using the find tool.
```css
/* || Text Styling */
```

### CSS Validation
Use [W3C CSS validator](https://jigsaw.w3.org/css-validator/) to make sure CSS is valid before pushing.

### !important
Avoid using `!important` whenever possible.
```css
.bad-code {
  /* Avoid */
  font-size: 4rem !important;
}
```

### CSS Comments
Use CSS-style comments to comment code that isn't self-documenting. Also note that you should leave a space between the asterisks and the comment. Put your comments on separate lines preceding the code they are referring to, like so:
```css
h3 {
  /* Creates a red drop shadow, offset 1px right and down, w/2px blur radius */
  text-shadow: 1px 1px 2px red;
  /* Sets the font-size to double the default document font size */
  font-size: 2rem;
}
```
### Declaration Stops
Use `;` after declaration (even the last one) for clarity.
```css
/* Avoid */
.test {
  display: block;
  height: 100px
}

/* Recommended */
.test {
  display: block;
  height: 100px;
}
```

### Property Name Stops
Use a space to separate property rule and values for clarity.
```css
/* Not recommended */
h3 {
  font-weight:bold;
}

/* Recommended */
h3 {
  font-weight: bold;
}
```
### Rule Separation
Always put a blank line between rules for clarity/
```css
html {
  background: #fff;
}

body {
  margin: auto;
  width: 50%;
}
```

### Double Quotes around values
Where quotes can or should be included, use them, and use double quotes. For example:
```css
[data-vegetable="liquid"] {
  background-color: goldenrod;
  background-image: url("../../media/examples/lizard.png");
}
```

### Shorthand vs Longhand
Use longhand instead of shorthand when possible for clarity and to avoid issues where values must be in a certain order.
```css
/* Use Longhand: */
font-variant: small-caps;
font-weight: bold;
font-size: 2rem;
line-height: 1.5;
font-family: sans-serif;
/* Instead of Shorthand: */
font: small-caps bold 2rem/1.5 sans-serif;
```
### Selectors
### ID Selectors
Avoid using ID selectors when possible because they are:
- less flexible; you can't add more if you discover you need more than one.
- harder to override because they have higher specificity than classes.
- 
### Type Selectors
- Unless necessary (for example with helper classes), do not use element names in conjunction with classes.
- Avoiding unnecessary ancestor selectors is useful for performance reasons.
```css
/* Avoid: */
ul.example {}
div.error {}

/* Recommended */
.example {}
.error {}
```
### Units
### Relative vs Absolute Units
Use relative units instead of absolute units whenever possible.
```css
/* Avoid */
font-size: 14px;

/* Recommended */
font-size: 2rem;
```
### Values to turn off properties
Use `0` instead of `none`
```css
border: 0;
```

### Declaration Order
- Alphabetize declarations
- Sort declarations consistently within a project. In the absence of tooling to automate and enforce a consistent sort order, consider putting declarations in alphabetical order in order to achieve consistent code in a way that is easy to learn, remember, and manually maintain.
- Ignore vendor-specific prefixes for sorting purposes. However, multiple vendor-specific prefixes for a certain CSS property should be kept sorted (e.g. -moz prefix comes before -webkit).
```css
background: fuchsia;
border: 1px solid;
-moz-border-radius: 4px;
-webkit-border-radius: 4px;
border-radius: 4px;
color: black;
text-align: center;
text-indent: 2em;
```

## JavaScript Styling
### Variables
### Variable Names
- Use short identifiers, and avoid non-common abbreviations. Good variable names are usually between **3 to 10-character long**, but as a hint only. For example, `accelerometer` is more descriptive than abbreviating to `acclmtr` for the sake of character length.
- Try to use real-world relevant examples where each variable has clear semantics. Only fall back to placeholder names like `foo` and `bar` when the example is simple and contrived.
- Do not prefix the variable name with its type. For example, write `bought = true` rather than bBought = `bBought` or `name = "John Doe"` instead of `sName = "John Doe"`.
- For primitive values, use camelCase, starting with a lowercase character. Do not use _. Use concise, human-readable, and semantic names where appropriate. For example, use `currencyName` rather than `currency_name`.
  
**Use**:
```JavaScript
const playerScore = 0;
const speed = distance / time;
```
**Don't Use**:
```JavaScript
const thisIsaveryLONGVariableThatRecordsPlayerscore345654 = 0;
const s = d / t;
```
### Variable Declarations
- **Use** `let` and `const`. Avoid `const` whenever possible.
- If a variable will not be reassigned, prefer `const`, like so:
```JavaScript
  const name = "Shilpa";
  console.log(name);
```
- If you'll change the value of a variable, use `let` as shown below:
```JavaScript
let age = 40;
age++;
console.log("Happy birthday!");
```
- Declare one variable per line, like so:
```JavaScript
let var1;
let var2;
let var3 = "Apapou";
let var4 = var3;
```
### Strings
Both single quotes and double quotes can be used for string literals, but prefer using double quotes `"a String" when possible.
### Template Literals
For inserting values into strings, **use** template literals. Their use prevents a lot of spacing errors:
```JavaScript
const name = "Shilpa";
console.log(`Hi! I'm ${name}!`);
```
**Avoid** concatenating strings like so:
```JavaScript
const name = "Shilpa";
console.log("Hi! I'm" + name + "!"); // Hi! I'mShilpa!
```
**Don't** overuse template literals. If there are no substitutions, use a normal string literal instead:
```JavaScript
const name = `John`; // Use double quotes instead
```
### Operators
- **Use** the strict equality and inequality operators like this:
```JavaScript
name === "Shilpa";
age !== 25;
```
- **Don't** use the loose equality and inequality operators, as shown below:
```JavaScript
name == "Shilpa";
age != 25;
```
### Objects
- When defining a class, **use PascalCase** (starting with a capital letter) for the class name and camelCase (starting with a lowercase letter) for the object property and method names.
- When defining an object instance, either a literal or via a constructor, **use camelCase**, starting with lower-case character, for the instance name. For example:
```JavaScript
const hanSolo = new Person("Han Solo", 25, "he/him");

const luke = {
  name: "Luke Skywalker",
  age: 25,
  pronouns: "he/him",
};
```
### Functions
- For function names, **use camelCase**, starting with a lowercase character. Use concise, human-readable, and semantic names where appropriate:
```JavaScript
function sayHello() {
  console.log("Hello!");
}
```
### Loops
- When iterating through all collection elements, avoid using the classical for `(;;)` loop; prefer `for...of` or `forEach()`.
Note that if you are using a collection that is not an Array, you have to check that `for...of` is actually supported (it requires the variable to be iterable), or that the `forEach()` method is actually present.
- **Use** `for...of`:
```JavaScript
const dogs = ["Rex", "Lassie"];
for (const dog of dogs) {
  console.log(dog);
}
```
- Or `forEach()`
```JavaScript
const dogs = ["Rex", "Lassie"];
dogs.forEach((dog) => {
  console.log(dog);
});
```
- **Avoid**:
```JavaScript
const dogs = ["Rex", "Lassie"];
for (let i = 0; i < dogs.length; i++) {
  console.log(dogs[i]);
}
```
- Make sure that you define the initializer properly by using the const keyword for for...of or let for the other loops. Don't omit it. These are correct examples:
```JavaScript
const cats = ["Athena", "Luna"];
for (const cat of cats) {
  console.log(cat);
}
```
- **Avoid**:
```JavaScript
const cats = ["Athena", "Luna"];
for (i of cats) {
  console.log(i);
}
```
### Comments
- If the purpose or logic of the code isn't obvious, add a comment with your intention, as shown below:
```JavaScript
let total = 0;

// Calculate the sum of the four first elements of arr
for (let i = 0; i < 4; i++) {
  total += arr[i];
}
```
- **Avoid** restating the code:
```JavaScript
let total = 0;

// For loop from 1 to 4
for (let i = 0; i < 4; i++) {
  // Add value to the total
  total += arr[i];
}
```
- Comments are also not necessary when functions have explicit names that describe what they're doing.
- In general, use single-line comments to comment code. Writers must mark each line of the comment with //, so that it's easier to notice commented-out code visually. In addition, this convention allows to comment out sections of code using /* … */ while debugging.
- Leave a space between the slashes and the comment. Start with a capital letter, like a sentence, but don't end the comment with a period:
```JavaScript
// This is a well-written single-line comment
```
- If a comment doesn't start immediately after a new indentation level, add an empty line and then add the comment. It will create a code block, making it obvious what the comment refers to.
Also, put your comments on separate lines preceding the code they are referring to. This is shown in the following example:
```JavaScript
function checkout(goodsPrice, shipmentPrice, taxes) {
  // Calculate the total price
  const total = goodsPrice + shipmentPrice + taxes;

  // Create and append a new paragraph to the document
  const para = document.createElement("p");
  para.textContent = `Total price is ${total}`;
  document.body.appendChild(para);
}
```
- Short comments are usually better, so try to keep them in one line of 60–80 characters. If this is not possible, use // at the beginning of each line:
```JavaScript
/ This is an example of a multi-line comment.
// The imaginary function that follows has some unusual
// limitations that I want to call out.
// Limitation 1
// Limitation 2
```
- **Don**'t use `/* … */`:
```JavaScript
/* This is an example of a multi-line comment.
  The imaginary function that follows has some unusual
  limitations that I want to call out.
  Limitation 1
  Limitation 2 */
```
