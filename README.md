# 3D Raycasting Engine<img width="2875" height="1612" alt="107834307-bd610300-6d8d-11eb-9d37-fc8a64efbe31" src="https://github.com/user-attachments/assets/39573953-fffe-4ff3-a230-813553991124" />


A real-time 3D rendering engine built in C using raycasting techniques, inspired by early first-person games such as Wolfenstein 3D.

This project focuses on low-level graphics programming, mathematical rendering systems, and performance-oriented software design without relying on modern graphics APIs.

---

## Overview

The goal of this project is to transform a 2D map into a dynamic 3D environment using raycasting. The engine simulates a first-person perspective by casting rays from the player’s position, calculating wall intersections, and rendering a 3D projection in real time.

This project was built entirely in C using MiniLibX and emphasizes understanding how real-time rendering systems work at a fundamental level.

---

## Core Features

### Rendering System

* Real-time raycasting engine
* 3D perspective projection from 2D maps
* Fish-eye distortion correction
* Texture mapping on walls
* Frame-based rendering loop

### Player System

* First-person camera control
* Smooth movement (WASD controls)
* Rotation system (left/right camera turning)
* Collision detection with map boundaries

### Map & Parsing System

* Custom `.cub` file parser
* Map validation (walls, structure, rules)
* Texture path loading
* Error detection and handling

### Engine Architecture

* Modular design separated by responsibility
* Clean rendering pipeline
* Organized memory management
* Event-driven input system

---

## Project Structure

```bash
.
├── includes/
│   └── cub3d.h
├── map/
│   └── *.cub maps
├── src/
│   ├── init_game/
│   ├── move/
│   ├── parsing/
│   ├── ray/
│   ├── render/
│   └── texture/
├── cub3d.c
└── Makefile
```

### Module Breakdown

| Module       | Responsibility                     |
| ------------ | ---------------------------------- |
| `init_game/` | Game initialization and setup      |
| `move/`      | Player movement and input handling |
| `parsing/`   | Map parsing and validation         |
| `ray/`       | Raycasting calculations            |
| `render/`    | Rendering pipeline                 |
| `texture/`   | Texture loading and management     |

---

## How It Works (Raycasting Logic)

Each frame, the engine performs the following steps:

1. Cast a ray for every vertical screen column
2. Detect intersection with walls
3. Compute distance from player to wall
4. Correct fish-eye distortion
5. Calculate projected wall height
6. Apply correct texture slice
7. Render final frame to the screen

This process creates the illusion of a 3D environment from a 2D map in real time.

---

## Controls

| Key | Action              |
| --- | ------------------- |
| W   | Move forward        |
| S   | Move backward       |
| A   | Strafe left         |
| D   | Strafe right        |
| ←   | Rotate camera left  |
| →   | Rotate camera right |
| ESC | Exit program        |

---

## Technologies Used

* C Programming Language
* MiniLibX (graphics library)
* X11 (window system)
* Make (build system)
* Linux environment

---

## Code Quality & Engineering Constraints

This project follows the **42 School Norminette coding standard**, which enforces strict rules to ensure clean, readable, and maintainable C code.

### Key Constraints Applied

* Functions limited in size (max 25 lines)
* Strict naming conventions and formatting rules
* No unused variables or redundant code
* Clear separation of responsibilities per module
* Structured and readable logic flow
* Modular design enforced by file organization

### Engineering Value

Although restrictive, these constraints improve real-world engineering skills:

* Forces modular and maintainable architecture
* Encourages clean function decomposition
* Improves debugging and traceability
* Builds discipline in low-level programming
* Simulates production-level code standards

---

## Skills Demonstrated

* Low-level C programming
* Graphics and rendering systems
* Raycasting and geometric computation
* Memory management
* Event-driven programming
* Software architecture design
* Performance optimization
* Parsing and validation systems

---

## Screenshots / Demo

Add screenshots or GIFs of gameplay here:

```
<img width="2875" height="1612" alt="render" src="https://github.com/user-attachments/assets/ad7ce06e-2be5-4578-bc07-ca4ea0dcaf7c" />

```

---

## Future Improvements

* Sprite rendering (objects inside the world)
* Floor and ceiling casting
* Dynamic lighting system
* Minimap integration
* Mouse-based camera control
* Advanced enemy AI system
* Performance optimizations (ray batching, caching)

---

## Learning Outcome

This project provides deep insight into how early 3D engines work internally, demonstrating how mathematical models, memory handling, and rendering loops combine to create real-time interactive environments.

It bridges the gap between theoretical computer graphics and practical system-level implementation.
