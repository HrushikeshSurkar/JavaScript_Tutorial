# Usage

> To use this code for learning purposes:
> Clone this repository.
> Open index.html in a web browser.
> Feel free to explore the code and experiment with JavaScript flow control concepts demonstrated in the video.
> follow the video guid [click here](https://youtu.be/atrYgwL5TsQ)

# License

> You can fill in the code sections as needed. If you have any specific instructions or details to add, feel free to customize the README accordingly.
<details>
# Video 8: Flow Control in JavaScript | if-else | switch

---

## Description:

In this GitHub guide, we delve into the core concepts of flow control in JavaScript, focusing on if-else statements and the switch case structure. Understanding these fundamentals is essential for effectively directing the behavior of your JavaScript programs based on specific conditions.

## HTML - index.html

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flow Control in JavaScript</title>
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <nav class="navBar">
      <ul class="navItemWrapper">
        <li class="navItem logo"><a class="navLink" href="#">Logo</a></li>
      </ul>
      <ul class="navItemWrapper">
        <li class="navItem"><a class="navLink" href="#">Home</a></li>
        <li class="navItem"><a class="navLink" href="#">Blog</a></li>
        <li class="navItem"><a class="navLink" href="#">Pricing</a></li>
        <li class="navItem"><a class="navLink" href="#">About</a></li>
      </ul>
      <ul class="navItemWrapper">
        <li class="navItem navButton login" id="login">
          <a class="navLink" href="#">Login</a>
        </li>
      </ul>
    </nav>
    <script src="script.js"></script>
  </body>
</html>
```

## CSS - style.css

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Arial", sans-serif;
  background-color: #f5f5f5;
  color: #333;
  margin: 0;
}

.navBar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #ffffff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.navItemWrapper {
  display: flex;
  align-items: center;
  list-style: none;
}

.navItem {
  margin: 0 15px;
  font-size: 16px;
  text-transform: uppercase;
  font-weight: 600;
  text-decoration: none;
  position: relative;
  transition: color 0.3s;
}

.navLink {
  color: #333; /* Default text color for navLink */
  text-decoration: none; /* No underline for navLink */
}

.navItem::after {
  content: "";
  display: block;
  height: 2px;
  width: 0;
  background-color: #4caf50;
  position: absolute;
  bottom: 0;
  left: 0;
  transition: width 0.3s;
}

.navItem:hover::after {
  width: 100%;
}

.logo {
  font-size: 24px;
  font-weight: bold;
  text-decoration: none;
}

.navButton {
  padding: 12px 24px;
  border-radius: 5px;
  background-color: #4caf50;
  color: white;
  cursor: pointer;
  text-decoration: none;
  transition: background-color 0.3s;
  border: none;
  font-size: 14px;
}

.navButton:hover {
  background-color: #45a049;
}
```

## JavaScript - script.js

#### **if Statement**

> **Description:** The if statement allows us to execute a block of code if a specified condition is true. In this example, we change the content of an HTML element based on a condition.
> **Example**

```
let login = "login";

if (login == true) {
  document.getElementById("login").innerHTML = "logout";
}
```

#### **if-else statement**

> **Description:** The if-else statement provides an alternative block of code to execute when the condition specified in the if statement is false. Here, we handle both true and false conditions.

#### Example

```
let login = "login";
if (login == true) {
  document.getElementById("login").innerHTML = "logout";
}
else {
  alert("invalid input");
}
```

#### **else-if ladder**

**Example**

```
let login = "login";

if (login == true) {
  document.getElementById("login").innerHTML = "logout";
} else if (login == false) {
  document.getElementById("login").innerHTML = "login";
} else if (login == 10) {
  document.getElementById("login").innerHTML = "10";
} else {
  alert("invalid input");
}
```

#### **switch case**

> **Description:** The switch case structure provides an efficient way to execute different blocks of code based on the value of an expression. Here, we demonstrate its usage to handle different cases.

```
let login = "login";
switch (login) {
  case "login":
    document.getElementById("login").innerHTML = "logout";
    break;
  case "logout":
    document.getElementById("login").innerHTML = "login";
    break;
  default:
    document.getElementById("login").innerHTML = "10";
    break;
}
```
</details>
# Video 9: Loops in JavaScript

---

## Introduction to Loops in JavaScript

> Loops in JavaScript are programming constructs that allow you to repeatedly execute a block of code until a specified condition is met. They are essential for automating repetitive tasks and iterating over data structures.
> Feel free to explore the code and experiment with JavaScript Loop concepts demonstrated in the video.
> follow the video guid [here](https://youtu.be/eCj2zypQZrk)

## Basic Setup

**HTML - index.html**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Loops Example</title>
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <div class="container">
      <h1>Loop Example</h1>
      <ul id="itemList"></ul>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

**CSS - style.css**

```css
body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 600px;
  margin: 50px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #f9f9f9;
}

h1 {
  text-align: center;
}

#itemList {
  list-style-type: none;
  padding: 0;
}

#itemList li {
  margin-bottom: 10px;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
  background-color: #fff;
}

#itemList li:last-child {
  margin-bottom: 0;
}
```

## For Loop

> The for loop in JavaScript is a powerful construct used to iterate over a range of values or elements. Here's how it works:

**Example**

```javascript
for (initialization; condition; increment) {
  //code to execute
}
```

#### In this syntax:

> **Initialization:** This part is executed before the loop starts. It typically initializes a counter variable.
> **Condition:** The loop continues executing as long as this condition evaluates to true.
> **Increment:** This part is executed after each iteration of the loop. It typically increments or decrements the counter variable.

**Example**

```
for (let i = 0; i <= 10; i++) {
  console.log(i);
}
```

## While Loop

> The while loop in JavaScript is another fundamental construct used to repeatedly execute a block of code as long as a specified condition is true. Here's how it works:

```
initialization
while (condition){
  // code to execute
  increment
}
```

#### In this structure:

> **Initialization :** This part is executed before the loop starts and typically initializes variables.
> **Condition :** The loop continues executing as long as this condition evaluates to true.
> **Increment :** This part is executed after each iteration and typically updates the variables involved in the condition.

#### Example

```
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}
```

This loop will print numbers from 1 to 5.

## Do-While Loop

> The do-while loop in JavaScript is similar to the while loop, but it guarantees that the code block is executed at least once before the condition is tested. Here's how it works:

#### Example

```
initialization
do {
  // code to execute
  increment
} while (condition)
```

In the do-while loop:

**Initialization:** This part is executed before the loop starts and typically initializes variables.
**Code to Execute:** The code block inside the loop is executed at least once.
Condition: The loop continues as long as this condition evaluates to true.
**Increment:** This part is executed after each iteration and typically updates the variables involved in the condition.

#### Example

```
let i = 1;
do {
console.log(i);
i++;
} while (i <= 5);
```

This loop will also print numbers from 1 to 5.

# Video 10 : Functions in JavaScript

---

## Introduction to Functions

> Functions are one of the fundamental building blocks in JavaScript, allowing you to encapsulate reusable pieces of code. They help make your code more organized, modular, and easier to maintain. Here's what you need to know about functions:

### Definition and Purpose

> A function is a block of code that performs a specific task or calculates a value. It's like a reusable recipe that you can call multiple times with different inputs, producing consistent outputs. Functions help you avoid repetitive code and promote code reuse and modularity.

### Syntax for Declaring and Calling Functions

> Function Declaration
> You can declare a function using the function keyword followed by the function name, parameters (if any), and the function body enclosed in curly
``` function functionName(parameter1, parameter2) {// function body}```

### Calling Functions

> To call or invoke a function, you simply write its name followed by parentheses ().
``` functionName(argument1, argument2); ```

#### Example

``` 
// Function declaration
function greet(name){
    return `Hello, ${name}!`;
}
// Calling the function
let message = greet('John');
console.log(message); // Output: Hello, John!
```

## Introduction to Function Expressions and Arrow Functions

In addition to function declarations, JavaScript also supports function expressions and arrow functions, which are more concise ways to define functions.

### Function Expression

A function expression defines a function as part of a larger expression or assigns it to a variable.

```
const functionName = function(parameter1, parameter2) {
// function body
};
```

### Arrow Function

Arrow functions provide a more concise syntax for defining functions, especially for simple one-liners. They use the arrow (=>) syntax.

```
const functionName = (parameter1, parameter2) => {
    // function body
};
```

#### Example:

```
// Function expression
const square = function(x) {
return x \* x;
};
// Arrow function
const cube = (x) => x _ x _ x;
```

Functions are a fundamental concept in JavaScript and mastering them will empower you to write more efficient and maintainable code.
