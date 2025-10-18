# Memory Game App

**Project Name:** Memory Game

## Table of contents
- [Overview](#overview)
- [Game Rules](#game-rules)
- [Core Features](#core-features)
- [Out of Scope](#out-of-scope)
- [Run the project locally](#run-the-project-in-locally)

## Overview

The Memory Game is a classic, browser-based card-matching game designed to be fun. The primary goal is to provide users a simple, challenging game to test and improve their memory and concentration skills. This project will serve as a showcase for modern frontend development practices, featuring a clean UI, smooth animations, and responsive design.

## Game Rules

The game consists of a grid of face-down cards. Each card has a matching pair. The player flips two cards per turn to find all the matches. The goal is to find all matching pairs.

**Core Rules:**
* A deck of identical card pairs is shuffled and displayed face-down in a grid.
* On each turn, a player flips two cards.
* If the two cards match, they remain face-up.
* If they don't match, they are flipped back face-down after a short delay.
* The game ends when all pairs have been found.

**Game Modes:**
* **Single-Player Mode**
  * The single-player version is a test of own memory and skill. To clear the entire board of all pairs in as few moves (or as little time) as possible.
  * **Scoring:** Performance is tracked by total moves and completion time. The goal is to minimize both.

* **Multiplayer Mode (Future Consideration)**
  * Max 4 players take turns.
  * If a player finds a match, they score a point and get another turn.
  * If not, the turn passes to the next player.
  * The player with the highest number of matched pairs win.

## Core Features

* **Responsive Game Board:**
  * Responsive card grid that works on desktop, tablet, and mobile.
  * Configurable grid sizes (e.g., 4x4, 6x6) for difficulty.
* **Game Logic:**
  * Card shuffle on game start.
  * Pair matching logic with visual feedback (match/no-match).
  * Game end detection (all pairs found).
* **Game Modes & Configuration:**
  * **Single-Player Mode:** Play against the clock and your own best score.
  * **Difficulty Settings:** Adjustable grid sizes (e.g., 4x4 for "Easy," 6x6 for "Hard").
* **Game State Tracking:** 
  * **Move Counter:** Counts the number of turns taken.
  * **Timer:** Tracks the elapsed time for the current game session.
* **User Controls:**
  * **Start/Restart Button:** Allows the user to begin a new game or reset the current one.
  * **New Game Button:** Starts a completely new game with a fresh set of cards.

## Out of Scope
The following features are explicitly not part of the initial release but can be considered for future versions:

* User leaderboards, or persistent score history.
* Customizable card themes (images/icons, colors) for the user to choose from.
* Complex animations or 3D effects.
* Multiplayer functionality.

## Run the project in locally

Clone this repository -

```sh
git clone https://github.com/sanjoypaul-git/memory-game.git
```

Go to the project directory

```sh
cd memory-game
```

install the dependencies

```sh
npm install
```

start the development server

```sh
npm run dev
```

Your app should be available in http://localhost:5173/
