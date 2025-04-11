# 🦖 Automated Dino Game Player

This Python script automates playing the Chrome Dino game hosted on [elgoog.im/dinosaur-game](https://elgoog.im/dinosaur-game/). It uses screen capturing and pixel analysis to detect obstacles and automatically jump over them in real time.

---

## 🧩 Features

- 📸 Captures a specific region of the screen to detect game objects
- 🎮 Automatically starts and plays the game
- 🌗 Adjusts behavior based on day/night mode
- ⚡ High refresh rate for smooth reaction (1000 FPS loop)

---

## 🚀 How It Works

1. Opens the Dino game in your browser in fullscreen mode.
2. Locates the top of the game field using an image reference (`top.png`).
3. Detects obstacles by analyzing grayscale pixels.
4. Presses the spacebar to jump when an obstacle is detected.

> 💡 The game reacts to the **difference** in pixel colors compared to the current background (day or night).

---

## 🖥 Requirements

- Python 3.10+
- [`pyautogui`](https://pypi.org/project/pyautogui/)
- [`Pillow`](https://pypi.org/project/Pillow/)
- [`ImageGrab`] (built into Pillow on Windows/macOS)
- A screenshot file named **`top.png`** which matches the header of the game screen

Install required libraries:

```bash
pip install pyautogui Pillow
```

---

## 📂 Usage

1. Make sure your screen resolution is high enough to run the browser in fullscreen.
2. Save a screenshot of the top of the game field as `top.png` in the same directory.
3. Run the script:

```bash
python main.py
```

4. The bot will automatically start playing the game.

---

## ⚠️ Notes

- The browser must open in **fullscreen mode** for coordinates to match.
- Timing may vary slightly depending on your system performance.
- The script uses pixel detection, so any theme or zoom changes might break detection.
- Works best on Windows/macOS (due to `ImageGrab` compatibility).