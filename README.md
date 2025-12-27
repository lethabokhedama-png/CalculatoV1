My v1 Calculator Project

Overview

This project is a simple web-based calculator built using HTML, CSS, and JavaScript. It performs basic arithmetic operations such as addition, subtraction, multiplication, and division. The goal of the project was to practice JavaScript fundamentals after learning the language and to understand how user input, DOM manipulation, and basic logic work together in a real project.

This calculator was designed to be responsive and mobile-friendly, meaning it works well on phones, tablets, and desktops without extra configuration.

Created by: Lethabo K


---

Time & Learning Context

Development time: Approximately 2 hours

Experience level: Built right after learning JavaScript

Process involved:

Learning core JavaScript syntax

Testing functions repeatedly

Fixing errors through trial and error

Connecting JavaScript logic to HTML buttons



This project focuses more on learning and understanding than advanced features.


---

Features

Clean calculator layout

Click-based input system

Supports decimals

Error handling for invalid expressions

Responsive layout using Flexbox and CSS Grid

Touch-friendly buttons for mobile devices



---

Project Structure

calculator/
│── index.html
│── style.css
│── main.js
│── README.md


---

How the Calculator Works

The calculator works by:

1. Displaying numbers and operators in an input field


2. Appending user input when buttons are clicked


3. Evaluating the full expression when = is pressed


4. Clearing the display when C is pressed



JavaScript controls the logic, HTML provides the structure, and CSS handles the design and responsiveness.


---

HTML Explanation

The HTML file defines the structure of the calculator.

Key Elements

#calculator: Main container

#display: Read-only input field that shows numbers and results

Buttons: Each button calls a JavaScript function using onclick


<input id="display" readonly>

The readonly attribute prevents users from typing manually

All input comes from button clicks


Each button calls a function like:

<button onclick="appendToDisplay('7')">7</button>

This sends the value to JavaScript.


---

CSS Explanation (Responsive Design)

The calculator layout uses Flexbox and CSS Grid to stay flexible on any screen size.

Centering the Calculator

body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

This ensures the calculator stays centered on all devices.

Button Grid

#keys {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
}

Automatically adapts to screen width

Keeps buttons evenly spaced


Mobile-Friendly Buttons

Large buttons

Rounded shape

High contrast colors

Easy to tap on touch screens



---

JavaScript Explanation

The JavaScript file controls all calculator logic.

Getting the Display Element

const display = document.getElementById("display");

This stores the display input so it can be updated dynamically.


---

appendToDisplay()

function appendToDisplay(input) {
  display.value += input;
}

Purpose:

Adds numbers or operators to the display

Called whenever a button is clicked



---

clearDisplay()

function clearDisplay() {
  display.value = "";
}

Purpose:

Clears the calculator screen

Resets the current expression



---

calculate()

function calculate() {
  try {
    display.value = eval(display.value);
  } catch (error) {
    display.value = "Error";
  }
}

Purpose:

Evaluates the full math expression

Uses eval() to compute the result

Catches errors if the expression is invalid



---

Error Handling

Invalid expressions show Error

Prevents the app from crashing

Keeps the calculator usable after mistakes



---

Limitations

Uses eval() (acceptable for learning, not ideal for production)

No keyboard input support

No advanced math functions



---

Possible Improvements

Replace eval() with a custom parser

Add keyboard support

Add percentage and power functions

Improve accessibility

Add dark/light theme toggle



---

Conclusion

This calculator project demonstrates a solid understanding of:

JavaScript functions

DOM manipulation

Event handling

Responsive UI design


It serves as a strong beginner project and a foundation for more complex JavaScript applications.


---

Author: Lethabo K
