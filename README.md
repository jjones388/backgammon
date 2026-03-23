# Backgammon

<img width="634" height="551" alt="backgammon_screenshot" src="https://github.com/user-attachments/assets/02cfea87-bc62-499f-92f6-29262d605bac" />


A fully playable single-page Backgammon game built with plain HTML, CSS, and JavaScript — no frameworks or dependencies required.

## Overview

This is a browser-based implementation of the classic board game Backgammon. You play as **White** against a computer opponent (**Black**). The goal is to move all your checkers around the board into your home quadrant and then bear them off before the computer does.

## Features

- Single-file implementation (`backgammon.html`) — open it in any browser and play instantly
- Visual board with alternating light/dark triangular points and a wooden aesthetic
- Animated dice rolling with doubles support (4 moves)
- Legal move highlighting — valid destination points pulse green when a checker is selected
- Hit and re-enter mechanics — blots (lone checkers) can be hit and sent to the bar
- Bear-off phase with a dedicated "Bear Off" zone in the side panel
- Computer AI that prioritizes bearing off, hitting blots, and advancing its furthest checkers
- Undo button to reverse your last move within a turn
- End Turn button to pass play to the computer
- Win/loss overlay with a "Play Again" option
- Off-checker tracking displayed in a side panel for both players

## How to Play

1. Open `backgammon.html` in any modern web browser.
2. Click **Roll Dice** to roll for your turn.
3. Click one of your **White** checkers to select it — valid destination points will pulse green.
4. Click a highlighted point (or the **Bear Off** zone) to move the checker.
5. Use **Undo** to take back a move within the same turn.
6. Click **End Turn** when you are done moving (or have no valid moves left).
7. The computer will then roll and move automatically.
8. First player to bear off all 15 checkers wins!

## Rules Implemented

- Standard starting position: 2 on point 24, 5 on point 13, 3 on point 8, 5 on point 6 (mirrored for Black).
- Checkers move in one direction only — White moves from low-numbered points toward high-numbered points and then bears off.
- Doubles grant four moves instead of two.
- A point occupied by two or more of your own checkers cannot be landed on by the opponent.
- A lone checker (blot) can be hit and sent to the bar; the hit player must re-enter from the bar before making any other moves.
- Bear-off begins once all 15 of your checkers are in your home board (points 19–24 for White).
- You may bear off with an exact die value, or use a higher die if no checker sits on a higher point.

## Computer AI

The computer uses a greedy heuristic to select moves each turn:

- Highest priority: bearing off checkers
- Second priority: hitting White blots
- Third priority: landing on empty points
- Fourth priority: building on existing stacks
- Prefers to move checkers that are furthest from home first

## Project Structure

```
backgammon/
└── backgammon.html   # Complete game — HTML, CSS, and JavaScript in one file
```

## Requirements

- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No server, build tools, or internet connection needed

## License

This project is released as open source. Feel free to fork, modify, and share.
