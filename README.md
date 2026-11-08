# 🏓 Pong: AI Edition

A modern take on the arcade classic **Pong**, built with **Python and Pygame**. Play against a computer-controlled paddle or a friend on the same keyboard, and set your own winning score from the main menu.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pygame](https://img.shields.io/badge/Library-Pygame-green)
![FPS](https://img.shields.io/badge/Runs%20at-60%20FPS-orange)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)

<!-- Add a gameplay GIF or screenshot here, e.g.
<p align="center"><img src="assets/preview.gif" alt="Pong gameplay" width="560"></p>
-->

---

## ✨ Features

- **Main menu** with mouse-hover buttons
  - **Single Player (vs AI)**
  - **Local Multiplayer** (two players, one keyboard)
- **Custom winning score:** click the input box and type any number (1–999, default **5**)
- **AI opponent** that tracks the ball whenever it is heading towards its side
- **Angle-based bounces:** where the ball hits the paddle changes its rebound angle, so you can aim your shots
- **Live scoreboard** and centre net
- **Winner screen:** "Player 1 Wins!", "Player 2 Wins!" or "AI Wins!", then back to the menu
- Smooth **60 FPS** gameplay on an 800×600 window

---

## 🚀 Getting Started

**Requirements:** Python 3.8+ and Pygame.

```bash
# 1. Download or clone this repository, then open the project folder
cd Pong_Game

# 2. Install Pygame
pip install pygame

# 3. Run the game
python "Pong Game - Source Code.py"
```

---

## 🎮 Controls

| Action | Player 1 (left) | Player 2 (right, multiplayer) |
| --- | --- | --- |
| Move up | `W` | `↑` |
| Move down | `S` | `↓` |

| Key | Action |
| --- | --- |
| `Esc` (in game) | Return to the main menu |
| `Esc` (in menu) | Quit |
| Any key / click (winner screen) | Back to the main menu |

In **Single Player** mode you control the left paddle and the AI controls the right one.

---

## 🧠 How It Works

- **Paddle, Ball and Button classes** keep the code organised.
- **Collision handling:** the ball bounces off the top and bottom walls; on a paddle hit its vertical speed depends on how far from the paddle's centre it struck:

```python
difference_in_y = middle_y - ball.y
reduction_factor = (paddle.height / 2) / ball.max_vel
ball.y_vel = -1 * (difference_in_y / reduction_factor)
```

- **AI:** when the ball moves towards it, the AI paddle moves to keep its centre within ±10 px of the ball.

---

## 🛠️ Tech Stack

- **Python 3**
- **Pygame:** rendering, input, timing and fonts

---

## 📂 Project Structure

```
Pong Game/
├── Pong Game - Source Code.py   # the full game (≈240 lines)
└── assets/                      # (add screenshots / GIF for this README)
```

---

## 🔮 Ideas for Future Improvements

- AI difficulty levels and ball speed-up on every rally
- Sound effects
- Pause menu
- Power-ups (bigger paddle, multi-ball)

---

## 👤 Author

**Somya Ranjan Sahoo** · [GitHub](https://github.com/somyaranjansahoo6422) · [Portfolio](https://somyaranjansahoo6422.github.io/projects/smaller-builds/)

If you like this project, consider giving it a ⭐!
