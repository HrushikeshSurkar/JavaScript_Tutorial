# Video 8: Flow Control in JavaScript | if-else | switch

## Usage

To use this code for learning purposes:

Clone this repository.
Open index.html in a web browser.
Feel free to explore the code and experiment with JavaScript flow control concepts demonstrated in the video.
follow the video guid [here](https://youtu.be/atrYgwL5TsQ)

## License

#### You can fill in the code sections as needed. If you have any specific instructions or details to add, feel free to customize the README accordingly.

### HTML - index.html

```html
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

### CSS - style.css

```css
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

### js - script.js

#### if

```
let login = "login";

if (login == true) {
  document.getElementById("login").innerHTML = "logout";
}

```

#### if else

```
let login = "login";

if (login == true) {
  document.getElementById("login").innerHTML = "logout";
}
else {
  alert("invalid input");
}
```

#### else if

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

#### Switch case

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

---

# Video 9: Loops in JavaScript

## Introduction to Loops in JavaScript

Loops in JavaScript are programming constructs that allow you to repeatedly execute a block of code until a specified condition is met. They are essential for automating repetitive tasks and iterating over data structures.
Feel free to explore the code and experiment with JavaScript Loop concepts demonstrated in the video.
follow the video guid [here](https://youtu.be/eCj2zypQZrk)

## Basic Setup

### HTML - index.html

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

# For Loop

The for loop in JavaScript is a powerful construct used to iterate over a range of values or elements. Here's how it works:

```javascript
for (initialization; condition; increment) {
  //code to execute
}
```

In this syntax:

**Initialization:** This part is executed before the loop starts. It typically initializes a counter variable.
**Condition:** The loop continues executing as long as this condition evaluates to true.
**Increment:** This part is executed after each iteration of the loop. It typically increments or decrements the counter variable.

#### For loop Example

```
for (let i = 0; i <= 10; i++) {
  console.log(i);
}
```

# While Loop

The while loop in JavaScript is another fundamental construct used to repeatedly execute a block of code as long as a specified condition is true. Here's how it works:

```
initialization
while (condition){
  // code to execute
  increment
}
```

In this structure:

**Initialization :** This part is executed before the loop starts and typically initializes variables.
**Condition :** The loop continues executing as long as this condition evaluates to true.
**Increment :** This part is executed after each iteration and typically updates the variables involved in the condition.

#### While Loop Example

```
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}
```

This loop will print numbers from 1 to 5.

# Do-While Loop

The do-while loop in JavaScript is similar to the while loop, but it guarantees that the code block is executed at least once before the condition is tested. Here's how it works:

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

#### Do-While Loop Example

```
let i = 1;
do {
console.log(i);
i++;
} while (i <= 5);
```

This loop will also print numbers from 1 to 5.
