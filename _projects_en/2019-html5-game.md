---
title: HTML5 Game
subtitle: Phaser 3-based merge puzzle game development
start_date: 2019-07-01
end_date: 2019-08-31
role: Web Game Developer
technologies:
  - HTML5
  - JavaScript
  - Phaser 3
---

## Project Overview

Developed a casual merge game that runs in browsers
using the HTML5-based game engine **Phaser 3**.
The game features a simple economy structure where players generate cakes,
merge identical cakes to upgrade them to higher levels, and sell completed cakes.

Supported both mobile browsers and PC with responsive game screens and touch controls.

## Core Features

- Cake merging (combining same-level cakes)
- Cake generation system
- Cake selling functionality
- Score and currency system
- Mouse/touch input support
- Responsive canvas UI

## Technical Implementation

### Game Engine / Logic

- Configured game loop and scenes based on Phaser 3
- Implemented cake object state (level), position, and movement animations
- Developed merge condition detection and upgrade logic
- Implemented in-game currency increase/decrease and selling logic

### UI / Interaction

- HTML5 canvas-based rendering
- Cake movement through touch/mouse dragging
- Designed cake slot structure and collision detection processing
- Implemented HUD (UI) displaying score and currency

### Performance & Platform Support

- Browser-focused optimization (FPS maintenance, object management)
- Responsive scaling for both mobile/PC playability
- Maintained fast loading speed with lightweight resources

## Achievements

- Completed solo development from game planning to implementation to testing within short period (2 months)
- Instantly playable in web browsers without separate installation
- Accumulated Phaser 3 usage experience and improved HTML5 game structure understanding
- Secured foundation technology for future casual game development through implementation of simple economy system and merge logic

## Technical Challenges & Solutions

Managing object collision and level-up timing became complex
when merge detection and drag movement occurred simultaneously.

To solve this:

- Unified cake object state management with **single State Manager**
- Optimized collision detection logic to check at "drop moment" instead of every frame
- Utilized Phaser's Scene structure to separate HUD, game logic, and effects for performance stabilization

As a result, completed a lightweight HTML5 casual game that implements the core fun of merge gameplay.
