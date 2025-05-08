# Team 10x Styling Guidelines
## Table of Contents
### [HTML](#html-styling)
### [CSS](#css-styling)
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

## CSS Styling

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
