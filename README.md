<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JavaScript Project Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1 id="main-title">Welcome to My JS Project</h1>
  <p id="message">Click the button below to run the script.</p>
  <button onclick="startDemo()">Run Script</button>
  <ul id="list"></ul>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
  background-color: #f0f0f0;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

ul {
  list-style: none;
  padding: 0;
}

// Part 1: Variable declarations and conditionals
let userName = "Alex";
let age = 20;

if (age >= 18) {
  console.log(`${userName} is an adult.`);
} else {
  console.log(`${userName} is a minor.`);
}

// Part 2: Custom functions

// Function 1 - Greet the user
function greetUser(name) {
  return `Hello, ${name}! Welcome to the JS demo.`;
}

// Function 2 - Add items to a list
function addItemsToList(items) {
  const list = document.getElementById("list");
  list.innerHTML = ""; // Clear existing list
  for (let item of items) {
    const li = document.createElement("li");
    li.textContent = item;
    list.appendChild(li);
  }
}

// Part 3: Loop examples

// Loop 1 - Simple for loop
function countToFive() {
  for (let i = 1; i <= 5; i++) {
    console.log("Count: " + i);
  }
}

// Loop 2 - Array iteration
const fruits = ["Apple", "Banana", "Cherry"];
for (let fruit of fruits) {
  console.log("Fruit:", fruit);
}

// Part 4: DOM interactions (3+)
function startDemo() {
  // DOM Interaction 1: Change text content
  document.getElementById("message").textContent = "Script is running...";

  // DOM Interaction 2: Change style
  document.getElementById("main-title").style.color = "green";

  // DOM Interaction 3: Update list with fruits
  addItemsToList(fruits);

  // Use a function
  alert(greetUser(userName));

  // Use a looped console log
  countToFive();
}



