# 🐍 Snake Workshop Documentation

## 📌 Description
In this workshop, you will build the classic **Snake game** using JavaScript and run it directly in your browser.  
Along the way, you’ll learn core programming concepts such as variables, functions, objects, and inputs.

By the end, you’ll have:
- A fully playable game  
- A better understanding of how interactive programs work  

**Language used:** JavaScript

---

## 🧰 Prerequisites
- A laptop *(can be provided during offline sessions)*  
- A code editor such as [Visual Studio Code](https://code.visualstudio.com/Download) or similar  
- The project repository downloaded and ready
- The [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VsCode.

---

## 🚀 Steps

### 1. Draw Gameboard  
**Concept:** Functions  

Create a function that draws the game area (grid) where the snake will move.

**You’ll learn:**
- How to define and call a function

---

### 2. Store Gameboard Variables  
**Concept:** Variables

Define variables for properties like:
- Width and height of the board
- Colors of game elements

**You’ll learn:**
- How to store and reuse values  
- Why variables make code flexible and easier to change  

---

### 3. Draw a Single Square  
**Concept:** Using variables  

Create a function to draw one square on the board using coordinates.

**You’ll learn:**
- How to pass parameters into functions  
- How small building blocks can be reused to build bigger features  

---

### 4. Create a Snake Object  
**Concept:** Objects  

Represent the snake as an object that contains:
- Its position (array of body parts)  
- Its direction  
- Its length  

**You’ll learn:**
- How to group related data  
- Why objects are useful for modeling real things in code  

---

### 5. Draw Snake  
**Concept:** Working with objects and arrays

Use the snake object to draw each part of the snake on the board.

---

### 6. Read User Input  
**Concept:** `if` conditions

Capture keyboard input (arrow keys) and change the snake’s direction.

**You’ll learn:**
- How to handle user input  
- How to use conditional logic (`if`) to control behavior  

---

### 7. Snake Movement  
**Concepts:** Functions & multiple conditions  

Update the snake’s position over time:
- Move the head forward  
- Shift the body  

---

### 8. Snake Movement at Edges  
**Concept:** `else` conditions  

Define what happens when the snake reaches the edge:
- Wrap around **or**  
- Stop the game  

**You’ll learn:**
- How to handle edge cases  
- How `if` / `else` structures control different outcomes  

---

### 9. Spawn Fruit  

Generate a fruit at a random position on the board.

---

### 10. Snake–Fruit Interaction  

Check if the snake eats the fruit.

---

### 11. Update Score  

Increase and display the score when the snake eats fruit.

---

### 12. Stop the Game  

End the game when:
- The snake hits itself  
- (Or another defined condition)

---

## 🧩 Available Functions

```javascript
function drawBoard(width, height, fillColor)
// Draws the gameboard with given dimensions and color

function drawSquare(left, top, fillColor)
// Draws a single square at a specific position

function drawScore(score)
// Displays the current score on screen

function drawSnakeBody(snakeBody, snakeBodyColour, snakeLength)
// Draws the snake using its body array and length

function getRandomNumber(min, max)
// Returns a random number between min and max (used for fruit spawning)

function snakeBodyMovement(snakeBody, snakeLength, snakeHead, fruitEaten)
// Updates the snake’s body positions and handles growth when fruit is eaten
```

## 💡 Don’t worry if everything doesn’t work immediately, debugging is part of programming.
