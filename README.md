# 🖱️ Mouseketeer

A small Windows desktop utility that keeps your PC awake by moving the mouse and right-clicking at a set interval, for a set length of time. Use it to stop the screen locking during long downloads, renders or test runs.

Built with Python, Tkinter, PyAutoGUI and pystray.

## Features

- Set the click interval (seconds) and the total run time (minutes)
- Shows a live countdown and has a **Stop** button
- Closing the window sends it to the system tray, with **Restore** and **Quit** options
- Ships as a standalone Windows executable, so you don't need Python

## How it works

Each cycle, Mouseketeer:

1. Moves the cursor to the top-left corner, then to the centre of the screen
2. Right-clicks at the centre
3. Moves the cursor to the bottom-right corner
4. Waits for the interval, then repeats until the run time ends or you press **Stop**

## Getting started

### Option 1: Executable (Windows)

1. Download [`mouseketeer_bot.zip`](mouseketeer_bot.zip) and extract it.
2. Run the executable inside.

### Option 2: From source

```bash
pip install pyautogui pystray pillow
python mouseketeer_bot.py
```

Run it from the repository folder, because the app loads `icon.ico` from the current directory.

## Usage

1. Enter the **Right-click interval** in seconds (default `30`).
2. Enter the **Total duration** in minutes (default `10`).
3. Click **Start**. The status line counts down the time left.
4. Click **Stop** to end early, or close the window to send it to the tray.

> **Note:** PyAutoGUI's fail-safe (move the mouse to a corner to abort) is turned off, because the app moves the cursor to the corners itself. Stop it with the **Stop** button or **Quit** from the tray menu.

## Disclaimer

The right-click lands in the middle of your screen, so pause Mouseketeer while you work. Use it responsibly and within your organisation's policies.
