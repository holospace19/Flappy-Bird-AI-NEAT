#Flappy Bird AI (NEAT)

An AI-powered version of the classic **Flappy Bird** game built with **Python**, **Pygame**, and **NEAT (NeuroEvolution of Augmenting Topologies)**.

![demo clip](\demo\rec1p.mp4)
---

## 📑 Table of Contents

* [Introduction](#introduction)
* [Features](#features)
* [Project Structure](#project-structure)
* [Installation](#installation)
* [Usage](#usage)
* [Dependencies](#dependencies)
* [Credits](#credits)
* [License](#license)

---
## Introduction

This project uses **NEAT-Python** to evolve neural networks that control birds in a Flappy Bird–style environment.
Each bird receives game-state inputs (position relative to pipes) and decides whether to jump. Over generations, better-performing networks survive and improve.

The game includes:

* Pixel-perfect collision detection
* Real-time training visualization
* Saving the best-performing neural network

## Features

* AI-controlled gameplay using NEAT
* Classic Flappy Bird mechanics
* Evolutionary learning over generations
* Fitness tracking and statistics
* Save & reuse the best neural network
* Network and training visualizations

---

## Project Structure

```
.
├── flappy_bird.py           # Main game & NEAT training loop
├── config-feedforward.txt   # NEAT configuration file
├── visualize.py             # Training & neural network visualization tools
├── requirements.txt         # Python dependencies
├── best.pickle              # Saved best neural network (auto-generated)
├── imgs/                    # Game assets (bird, pipes, background, base)
└── README.md
```

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/flappy-bird-neat.git
cd flappy-bird-neat
```

### 2. Create a virtual environment (optional but recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Usage

Run the training simulation:

```bash
python flappy_bird.py
```

The NEAT algorithm will:

* Spawn a population of birds
* Evaluate fitness based on survival and pipes passed
* Evolve better networks over generations
* Save the best-performing network to `best.pickle`

---

## Configuration

The NEAT parameters are defined in:

```
config-feedforward.txt
```

Key settings include:

* Population size: `50`
* Activation function: `tanh`
* Inputs: `3`
* Outputs: `1`
* Feed-forward networks only
* Structural mutations enabled

You can tweak mutation rates, population size, or fitness thresholds to experiment with learning behavior.

---

## Dependencies

* `pygame`
* `neat-python`
* `numpy`
* `matplotlib`
* `graphviz`

---

## Credits

* Original Flappy Bird concept by **Dong Nguyen**
* NEAT algorithm by **Kenneth O. Stanley**
* Python implementation via **neat-python**
* Background image made using AI

---

## 📜 License

This project is licensed under the **MIT License**.
You are free to use, modify, and distribute this project with attribution.

