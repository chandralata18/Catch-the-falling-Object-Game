# Catch-the-falling-Object-Game

A lightweight browser game where players control a basket to catch falling apples.
The objective is simple: catch as many apples as possible while avoiding misses. As your score increases, the apples fall faster, making the game progressively more challenging.

This project is implemented as a single-file, zero-dependency web game, making it extremely easy to run, modify, and deploy.

---

🎮 Key Features

Progressive Difficulty
  Apple fall speed increases as the score grows, making gameplay more challenging over time.

High Score Persistence
  High scores are stored using `localStorage`, so the best score remains saved between sessions.

Responsive Design
  Works smoothly across desktop and mobile devices with adaptive UI scaling.

Pause & Restart Controls

  Pause or resume gameplay instantly.
  Restart the game anytime.

Touch & Mouse Support
  The basket can be controlled using both mouse movement and touch gestures.

Dynamic Apple Spawning
  Apples spawn randomly across the top of the screen for unpredictable gameplay.

---

🕹️ How to Play

Controls

| Action         | Control                     |
| -------------- | --------------------------- |
| Move Basket    | Move mouse horizontally     |
| Mobile Control | Drag finger across screen   |
| Pause / Resume | `Space` key or Pause button |
| Restart Game   | `R` key or Restart button   |

Objective

1. Move the basket to **catch falling apples**.
2. Each caught apple **increases your score**.
3. Missing apples **reduces lives**.
4. The game ends when **all lives are lost**.

---

🧰 Tech Stack

This project is built using:

HTML5 – Game structure and layout
CSS3 – Styling, layout, and animations
Vanilla JavaScript – Game logic and interactivity
SVG – Basket graphics

Zero Dependency Project

The game does not rely on any external libraries or frameworks. Everything runs inside a single `.html` file.

---

⚙️ Game Logic Overview

 Main Game Loop

The game uses `requestAnimationFrame()` to continuously update the game state.

Each frame:

1. New apples may spawn.
2. Existing apples move downward.
3. Collision detection runs.
4. Missed apples reduce lives.

---

Collision Detection (AABB)

The game uses Axis-Aligned Bounding Box (AABB) collision detection.

It compares the bounding rectangles of:

The basket
The falling apple

If the rectangles overlap, the apple is considered caught.

---

Dynamic Spawning System

Apple spawning frequency dynamically adjusts based on score.

Higher score → faster spawn rate
Apples also gain increased fall speed over time

This ensures progressive gameplay difficulty.

---

🚀 Installation / Setup

This project requires no installation or dependencies.

Run Locally

1. Download or clone the repository

```bash
git clone https://github.com/yourusername/catch-the-falling-apples.git
```

2. Open the file:

```
catch-the-falling-apples.html
```

3. Double-click the file or open it in any modern browser.

That's it — the game runs instantly.

---

🎨 Customization

Game behavior can be modified via the `CONFIG` object in the script.

Example configuration:

```javascript
const CONFIG = {
  appleSrc: "apple.png",
  basketWidth: 120,
  basketHeight: 80,
  initialLives: 3,
  initialSpawnInterval: 1100,
  spawnIntervalMin: 350,
  baseFallSpeed: 1.8,
  speedIncreasePerScore: 0.08,
  maxFallSpeed: 10.5,
  appleSize: 44
};
```

📄 License

This project is open-source and available under the **MIT License**.

---

