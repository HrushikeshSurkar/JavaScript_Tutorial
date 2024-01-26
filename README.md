# video 8 : flow control using if else and switch 

### index.html

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flow Control in JavaScript</title>
    <link rel="stylesheet" href="style.css">
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

### style.css

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
