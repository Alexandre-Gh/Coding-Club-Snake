# Introduction to programming in Javascript and Project Tutorial

This project is the starting point of a small Snake game. Some parts of the game engine are already handled for you, such as the main structure of the game loop and methods to draw on the screen data needed to keep track of the game state.

What remains is understanding how the code works and how to extend it. This document does not explain everything about JavaScript or game development. Instead, it focuses on a few essential programming concepts that appear directly in this project: variables, functions, and parameters.

These ideas are enough to get started, but not enough to go further on their own. As you continue, you will need to explore additional concepts and examples through practice and external learning.

---

## Variables: storing data

A **variable** is used to store data that your program can use later.

In JavaScript, variables are created using keywords such as `const` or `let`.

```javascript
const SQUARE_SIZE = 25;
```

This line can be separated into multiple parts:

- `const` is the keyword used to create the variable
- `SQUARE_SIZE` is the name of the variable
- `=` assigns a value to the variable
- `25` is the stored value

---

### Choosing a variable name

Variable names should describe what the value represents.

Good variable names:

```javascript
const playerSpeed = 10;
const snakeLength = 5;
const gameOver = false;
```

Bad variable names:

```javascript
const x = 10;
const thing = 5;
const data = false;
```

A clear variable name makes code easier to read and understand.

---

### `const` and `let`

`const` means the variable should not be reassigned later.

```javascript
const SQUARE_SIZE = 25;
```

Trying to change it later is not allowed:

```javascript
SQUARE_SIZE = 50;
```

For values that are meant to change during the game, `let` is used instead:

```javascript
let score = 0;

score = score + 10;
```

Here, the value stored in `score` changes over time.

---

### Variables can also store objects

A variable can store more than a single value.

```javascript
const game = {
    status: "playing",
    score: 0,
    speed: 100
}
```

This is called an **object**.

Inside the object:

- `status` stores the current game state
- `score` stores the player's score
- `speed` stores the game speed

You can access these values using a `.`:

```javascript
game.score = game.score + 10;
```

This increases the score by 10.

---

## Functions: reusable blocks of code

A **function** is a block of code that performs a specific task.

Functions are useful because they allow code to be reused instead of rewritten multiple times.

Here is a simple function:

```javascript
function drawSquare(x, y, color) {
    drawBoard(x, y, color);
}
```

This function can also be separated into different parts:

- `function` tells JavaScript that you are creating a function
- `drawSquare` is the function name
- `(x, y, color)` are the function parameters
- `{ }` contains the code that will run when the function is called

---

### Calling a function

Defining a function does not execute it automatically.

To run the function, it must be called:

```javascript
drawSquare(10, 20, "green");
```

The values passed into the function are called **arguments**.

In this example:

- `x` becomes `10`
- `y` becomes `20`
- `color` becomes `"green"`

Inside the function, these values can be used like normal variables.

---

### Parameters

Parameters are variables created by the function itself.

They only exist inside the function and receive values when the function is called.

Example:

```javascript
function showScore(score) {
    console.log(score);
}
```

Calling the function:

```javascript
showScore(100);
```

Inside the function, `score` now contains `100`.

Functions can have:

- no parameters
- one parameter
- multiple parameters

Examples:

```javascript
function startGame() {

}

function setSpeed(speed) {

}

function drawSquare(x, y, color) {

}
```

---

### Functions in this project

Some functions are already provided for you and will automatically be called by the game system:

```javascript
function loop() {

}

function draw() {

}

function onKeyDown(keyCode) {

}
```

Each function has a specific purpose:

- `loop()` updates the game logic repeatedly
- `draw()` renders the game on the screen
- `onKeyDown(keyCode)` reacts to keyboard input

The `keyCode` parameter contains information about the pressed key.

Example:

```javascript
onKeyDown(ARROW_UP);
```

Inside the function, `keyCode` will contain `ARROW_UP`.

This allows one function to handle all keyboard inputs.

⚠️ Check the provided documentation to see which predefined variables and key codes are available.

---