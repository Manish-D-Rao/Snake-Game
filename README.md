🐍 README: Snake io Game 🎮
---

This is a simple implementation of the classic **Snake io** game using **HTML, CSS, and JavaScript**.

## 🚀 Getting Started

To play the game, simply open the `index.html` file in your web browser.

### Prerequisites

You need a modern web browser (like Chrome, Firefox, Edge, etc.) to run the game.

### Files

* `index.html`: The main HTML structure of the game, including the game board, score displays, and modal windows.
* `style.css`: Contains all the styling for the game, utilizing CSS variables for color and spacing management.
* `script.js`: The core JavaScript logic that handles game mechanics, snake movement, food generation, collision detection, and score tracking.

## 🕹️ How to Play

1.  **Open `index.html`** in your browser.
2.  Click the **"Start Game"** button to begin.
3.  Control the snake's direction using the **Arrow Keys** (Up, Down, Left, Right) on your keyboard.
4.  The goal is to move the snake to consume the **food** (red block) to grow and increase your score.
5.  The game ends if the snake hits the **boundaries** of the board.

## ✨ Features

* **Classic Snake Gameplay**: Move a growing snake to eat food.
* **Score Tracking**: Keep track of your current **Score** and the **High Score** (persisted using `localStorage`).
* **Time Tracking**: Displays the elapsed time of the current game session.
* **Start/Game Over Modals**: User-friendly screens for starting and restarting the game.
* **Responsive Grid**: The game board is dynamically sized based on the container, creating a grid of blocks.
* **Custom CSS Variables**: Clean and manageable styling with defined CSS variables for colors, spacing, and border radii.

## 🛠️ Code Overview

### HTML (`index.html`)

Sets up the basic layout, including sections for `infos` (score, time) and the `board` (game area), and a full-screen `modal` for game state messages.

### CSS (`style.css`)

Utilizes a dark theme with bright accents:
* Sets up global reset and basic `html`/`body` styling.
* Defines **CSS variables** (`:root`) for easy theme modification.
* Uses **Flexbox** for layout in the `section` and **CSS Grid** for the `board`.
* Defines classes for the snake's body (`.fill`) and the food (`.food`).

### JavaScript (`script.js`)

Handles the game logic:

* **Initialization**: Calculates the number of rows and columns based on the board's size and block dimensions. Initializes the snake's position and the first food location.
* **`render()` Function**: The main game loop executed at an interval (`200ms`).
    * Calculates the **new head position** based on the current `direction`.
    * Checks for **boundary collision** (Game Over).
    * Handles **food consumption**: Generates new food, grows the snake, updates the score, and checks for a new high score.
    * **Updates the board** by shifting the snake's segments.
* **Movement**: Uses the `keydown` event listener to update the `direction` variable based on arrow key presses.
* **Modals & Controls**: Manages the display of start/game over screens and handles the "Start Game" and "Restart Game" button clicks, setting up/clearing the game intervals (`intervalID` for movement, `timeIntervalID` for clock).
* **High Score**: Uses `localStorage` to save and display the high score across sessions.

## 🧑‍💻 Contributing

Feel free to fork the repository, open issues, or submit pull requests with improvements or new features!
