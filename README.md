# Usage

> To use this code for learning purposes:
> Clone this repository.
> Open index.html in a web browser.
> Feel free to explore the code and experiment with JavaScript flow control concepts demonstrated in the video.
> follow the video guid [click here](https://youtu.be/atrYgwL5TsQ)

# License

> You can fill in the code sections as needed. If you have any specific instructions or details to add, feel free to customize the README accordingly.

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
> ` function functionName(parameter1, parameter2) {// function body}`

### Calling Functions

> To call or invoke a function, you simply write its name followed by parentheses ().
> `functionName(argument1, argument2);`

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

### Arrow Function
Arrow functions provide a concise syntax for defining functions, particularly useful for simple one-liners. They use the arrow (=>) syntax.
#### Example in JavaScript:
```
const greet = (name) => {
    return "Hello, " + name + "!";
};

// Calling the function
console.log(greet("John")); // Output: Hello, John!
```
> In this example, greet is a variable that holds an arrow function. It takes a parameter name and returns a greeting message. Arrow functions are handy for writing compact and readable code.

## What is a Function Expression?
A function expression in programming allows you to define a function as a value within an expression. This means you can assign a function to a variable or pass it as an argument to another function, treating it like any other data type.
>Example in JavaScript
```
// Function expression
var greet = function(name) {
    return "Hello, " + name + "!";
};

// Calling the function
console.log(greet("John")); // Output: Hello, John!

```
>In this example, greet is a variable that holds a function. This function takes a parameter name and returns a greeting message. Function expressions are useful for creating anonymous functions or passing functions as arguments to other functions.

### Leap Year code

> HTMl code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Leap Year Checker</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>Leap Year Checker</h1>
    <input type="number" id="year" placeholder="Enter a year" />
    <button onclick="checkLeapYear()">Check</button>
    <div id="result"></div>
  </body>
</html>
```

> CSS code

```css
body {
  font-family: Arial, sans-serif;
  text-align: center;
}
#result {
  font-size: 24px;
  margin-top: 20px;
}
```

> js code

```js
function checkLeapYear() {
  var year = document.getElementById("year").value;
  var result = document.getElementById("result");

  if (year % 4 === 0 && (year % 100 !== 0 || year % 400 === 0)) {
    result.textContent = year + " is a leap year!";
  } else {
    result.textContent = year + " is not a leap year.";
  }
}
```


# Video 11 : Quiz Application

---

## Introduction

The Quiz Application allows users to:

- Start the quiz.
- Answer multiple-choice questions.
- Submit answers and receive feedback.
- Track their score.
- Restart the quiz if desired.
- It's a simple web-based quiz implemented using HTML, CSS, and JavaScript.

## Steps to Crate Quiz Application

### Step 1 : Analyze the Problem

**Objective:** Create a simple web application that allows users to take a quiz by answering a single question.

**Features:**

- The application should display a start button prompting the user to begin the quiz.
- Upon clicking the start button, the application should display a question along with multiple-choice options.
- Users should be able to select one option as their answer.
- After selecting an option, the user should be able to submit their answer.
- Upon submission, the application should provide feedback indicating whether the answer was correct or incorrect.
- The application should keep track of the user's score.
- After answering the question, the user should have the option to restart the quiz.
- The application should display the user's score at the end of the quiz.

### Step 2 : Start Building

- Create an HTML file (index.html) with the necessary structure, including div elements for displaying the question, options, feedback, score, and buttons.
- Link a CSS file (style.css) to style the appearance of the quiz interface.
- Write JavaScript code (script.js) to implement the quiz functionality.
- Define variables to store references to HTML elements such as the question, options, feedback, score, and buttons.
- Implement functions to handle starting the quiz, displaying the question, checking the answer, displaying feedback, updating the score, and restarting the quiz.
- Add event listeners to the start button, submit button, and restart button to trigger the corresponding functions when clicked.
- Define an array or object to store quiz questions along with their options and correct answers.
- Update the question and options dynamically based on the current question index.
- Compare the user's selected answer with the correct answer to determine if it is correct or incorrect.
- Display appropriate feedback and update the score accordingly.
- Allow the user to restart the quiz by resetting the score and displaying the start button again.

### Step 3 : Testing

- Test the application thoroughly to ensure all features work as expected.
- Verify that the quiz starts correctly, displays questions and options, accepts user input, provides feedback, updates the score, and allows the user to restart the quiz.
- Test edge cases such as selecting no option, selecting incorrect options, and restarting the quiz multiple times.
- Ensure the application is responsive and works well on different devices and screen sizes.

### Step 4 : Deployment

- Host the application on a web server or deploy it to a hosting platform to make it accessible online.
- Share the link with users to allow them to take the quiz.

## Solution Link

[Github](https://github.com/HrushikeshSurkar/QuizApplication)

## Video Guide
[Youtube](https://youtu.be/wsTDJ2H1mo4?si=_C_Zj_cY6cb3ywm2)


# Video 12 : Mastering Scope and Closures in JavaScript

Welcome back, JavaScript enthusiasts! Today, we're diving deep into two fundamental concepts: scope and closures. Understanding these concepts is crucial for writing clean, efficient JavaScript code. So grab your favorite beverage, sit back, and let's get started!

## Why Scope and Closures Matter

Before we jump into the nitty-gritty details, let's talk about why scope and closures matter in JavaScript. Scope determines the accessibility of variables and functions in your code, while closures allow inner functions to access variables from their outer scope. These concepts are essential for writing code that's easier to understand, maintain, and debug."

## Introduction to Scope

Let's start with scope. In JavaScript, scope defines where variables and functions are accessible within your code.

Variables declared outside of any function are in the global scope, meaning they can be accessed from anywhere in your code. On the other hand, variables declared within a function are in the local scope and can only be accessed within that function.

#### Code Example:

```javascript
var globalVar = "I'm global";
function accessGlobal() {
  console.log(globalVar); // Accessing global variable
}
accessGlobal(); // Output: I'm global
```

## Exploring Closures

Now, let's explore closures. Closures allow inner functions to retain access to variables from their lexical scope, even after the outer function has finished executing.

This means that inner functions 'remember' and can still use variables from their outer scope, even if those variables are no longer in scope.

#### Code Example:

```javascript
function outerFunction() {
  var outerVar = "I'm outer";
  function innerFunction() {
    console.log(outerVar); // Accessing outer function's variable
  }
  return innerFunction;
}

var closureFunc = outerFunction();
closureFunc(); // Output: I'm outer
```

#### Practical Examples

To solidify our understanding, let's dive into some practical examples.

We'll explore how scope and closures are used in everyday JavaScript programming, from managing variable access to creating encapsulated functionality.

#### Code Example:

```javascript
var counter = (function () {
  var count = 0;

  return function () {
    return ++count;
  };
})();

console.log(counter()); // Output: 1
console.log(counter()); // Output: 2
```

## Conclusion

And there you have it! Scope and closures are fundamental concepts in JavaScript that every developer should master.

By understanding how scope works and leveraging closures effectively, you'll be well-equipped to write cleaner, more maintainable JavaScript code.

Thanks for tuning in! Don't forget to like, subscribe, and hit that notification bell for more JavaScript tips and tutorials. Until next time, happy coding!

