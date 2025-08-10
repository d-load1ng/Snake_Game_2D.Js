# 🐍 Snake Game 2D

A classic Snake game implementation using vanilla JavaScript, HTML5 Canvas, and CSS.

![Snake Game Screenshot](https://user-images.githubusercontent.com/82943826/235201219-c93b5e4e-0e6a-4d1f-86d7-2eb24f30243d.png)

## 🎮 Demo

To play the game:

1. Clone this repository
2. Run `npm install` to install dependencies
3. Run `npm start` to start the local server
4. Open your browser and navigate to `http://localhost:8080`

## 🕹️ How to Play

- Use the arrow keys to control the snake
- Eat the red food to grow longer and earn points
- Avoid hitting the walls, obstacles, and yourself
- The game speeds up every 3 points, increasing difficulty

## 🔧 Technical Implementation

### Architecture

The game is built using an object-oriented approach with the following key classes:

- `Snake`: Manages the snake's body, color, and direction
- `Food`: Handles food generation and positioning
- `Walls`: Creates and manages obstacles
- `Cell`: Basic grid cell representation
- `Game`: Core game engine that coordinates all components

### Key Features

#### 🐍 Snake Mechanics

```javascript
class Snake {
  constructor() {
    this.body = [
      { x: 150, y: 150 },
      { x: 140, y: 150 },
      { x: 130, y: 150 },
    ];
    this.color = "green";
    this.direction = "R";
  }
}
```

The snake is represented as an array of body segments. The first element is the head, which leads the movement. When the snake moves, a new head is added in the direction of movement, and the tail is removed unless the snake eats food.

#### 🍎 Dynamic Food Generation

```javascript
setRandomPosition() {
  this.x = this.setRandomPoint();
  this.y = this.setRandomPoint();
}

setRandomPoint() {
  return Math.round((Math.random() * (300 - 10) + 10) / 10) * 10;
}
```

Food is randomly positioned on the canvas using a grid-aligned system to ensure food aligns perfectly with the snake's movement.

#### 🏆 Progressive Difficulty

```javascript
if (this.score % 3 === 0) {
  this.clockSpeed -= this.clockDecrement;
  clearInterval(this.timer);
  this.timer = setInterval(this.clockClick.bind(this), this.clockSpeed);
  this.level += 1;
}
```

The game increases in difficulty by speeding up every 3 points earned, creating an increasingly challenging experience.

#### 🧱 Obstacle System

```javascript
class Walls {
  constructor() {
    this.color = "white";
    this.bricks = [
      { x: 200, y: 200 },
      { x: 190, y: 200 },
      // More wall positions...
    ];
  }
}
```

Static obstacles are placed on the game board, adding complexity to navigation.

#### 🎮 Collision Detection

The game implements comprehensive collision detection for:
- Self-collision (snake hitting itself)
- Wall collision
- Obstacle collision
- Food collection

#### 🏁 Game Over & Reset

```javascript
resetGame() {
  this.clockSpeed = this.clockSpeedInitial;
  clearInterval(this.timer);
  this.timer = setInterval(this.clockClick.bind(this), this.clockSpeed);
  this.vel = { x: 10, y: 0 };
  this.score = 0;
  this.snake = new Snake();
  this.food = new Food();
  // More reset logic...
}
```

Complete game reset functionality allows for seamless replay after game over.

## 🎨 Visual Design

The game features:
- Custom pixel font styling
- Retro-style UI with glowing effects
- Grid-based movement
- Score and level display
- High score tracking

## 🛠️ Technical Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Rendering**: HTML5 Canvas
- **Build/Dev**: Node.js with http-server for local development
- **Dependencies**: No external libraries for game logic - pure vanilla JS

## 🔄 Game Loop

The game utilizes a timer-based game loop system:

```javascript
clockClick() {
  this.generateMove();
  this.checkGrow();
  this.GameOver();
  // Drawing operations
  this.clearCanvas();
  this.drawWalls();
  this.drawSnake();
  this.drawFood();
  this.drawScore();
  this.drawHighScore();
  this.drawLevel();
}
```

This function handles all game state updates and rendering operations on each clock cycle.

## 📐 Customization

The game can be easily customized by modifying:
- Canvas dimensions
- Snake speed and growth
- Obstacle layouts
- Difficulty progression
- Visual styling through CSS

## 📋 Future Enhancements

Potential improvements that could be added:
- Mobile touch controls
- Power-ups and special food items
- Multiple game modes
- Leaderboard system
- Sound effects and music

## 📄 License

ISC License - See LICENSE file for details.
