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

Example:

```javascript
const playerSpeed = 10;
const snakeLength = 5;
const gameOver = false;
```

A clear variable name makes code easier to read and understand.

---

### `const` and `let`

`const` means the variable is constant and cannot be changed after creation.

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

You can access these values like this:

```javascript
game.score = game.score + 10;
```

This example code increases the score by 10.

---

## Functions: reusable blocks of code

A **function** is a reusable block of code that performs a task.

Functions are useful because they allow the same code to be executed multiple times without rewriting it.

Here is a complete example:

```javascript
let result = 0; //An external variable in the context of this example

function addNumbers(a, b) {
    result = a + b;
}
```

This function can be separated into several parts:

- `function` tells JavaScript that a function is being created
- `addNumbers` is the name of the function
- `a` and `b` are called **parameters**
- `{ }` contains the code that will run when the function is called

The parameters (`a` and `b`) are variables created by the function itself.  
They receive values when the function is called.

Example:

```javascript
addNumbers(5, 3);
```

When this function call happens:

- `a` receives the value `5`
- `b` receives the value `3`

So inside the function, the code becomes:

```javascript
result = 5 + 3;
```

After the calculation, `result` will contain `8`.

This allows the same function to work with different values without rewriting the logic every time.

For example:

```javascript
addNumbers(10, 2);
addNumbers(7, 1);
addNumbers(100, 50);
```

Each function call uses different values while reusing the same code structure.

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

This values can either be:

```javascript
ARROW_UP
ARROW_DOWN
ARROW_RIGHT
ARROW_LEFT
```

⚠️ Check the provided documentation to see which predefined variables and key codes are available.

---