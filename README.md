# Flappy Bird AI using NEAT Algorithm

## Overview

This project implements an AI-driven version of the classic Flappy Bird game using the **NEAT (NeuroEvolution of Augmenting Topologies)** algorithm. The AI learns to play Flappy Bird by evolving neural networks over generations, optimizing its performance to achieve the highest possible score. The project is built using Python, Pygame for rendering the game, and the NEAT library for the AI logic.

## Features

- **AI-Driven Gameplay**: The AI learns to play Flappy Bird using a neural network that evolves over generations.
- **NEAT Algorithm**: The NEAT algorithm is used to evolve the neural networks, allowing the AI to improve its performance over time.
- **Real-Time Visualization**: The game is rendered in real-time using Pygame, allowing you to watch the AI learn and improve.
- **Customizable Configuration**: The NEAT algorithm's parameters can be customized in the `config_feedforward.txt` file to fine-tune the AI's learning process.
- **Score Tracking**: The game tracks the score and the current generation, displaying them on the screen.

## Prerequisites

Before running the project, ensure you have the following installed:

- **Python 3.7 or higher**
- **Pygame**: For rendering the game.
- **NEAT-Python**: For implementing the NEAT algorithm.

You can install the required libraries using pip:

```bash
pip install pygame neat-python
```

##Project Structure

```bash
flappy-bird-ai/
├── flappy_bird.py
├── config_feedforward.txt
├── imgs/
│   ├── bird.png
│   ├── base.png
│   ├── pipe.png
│   └── bg.png
└── requirements.txt
```

flappy_bird.py: The main script that runs the Flappy Bird game and implements the NEAT algorithm.
config_feedforward.txt: Configuration file for the NEAT algorithm.
imgs/: Folder containing all game assets (images of bird, background, pipes, base, etc.).
requirements.txt: File listing all Python dependencies.

## Installation
1. Clone the Repository
```bash
git clone https://github.com/your-username/flappy-bird-ai.git
cd flappy-bird-ai
```
2. Install Dependencies
```bash
pip install -r requirements.txt
```
2. Install Dependencies
```bash
pip install -r requirements.txt
```
3. Run the Game
```bash
python flappy_bird.py
```

## How it works

How It Works
NEAT Algorithm

The NEAT algorithm is a genetic algorithm that evolves neural networks over generations. It begins with a population of simple networks and increases complexity by adding nodes and connections. The fittest networks (those achieving the best performance in the game) are selected for reproduction, and their offspring inherit and mutate traits.
Game Mechanics

    Bird: Controlled by the neural network, it decides when to jump based on environment inputs.
    Pipes: Act as obstacles. The bird must pass between them without hitting.
    Base: The ground the bird must avoid crashing into.
    Score: Increases with each pipe successfully passed.

Neural Network Inputs

Each bird's neural network receives the following inputs:

    Bird's Y-position
    Distance to the top pipe
    Distance to the bottom pipe

Fitness Function

The fitness of each bird is based on:

    Time survived
    Number of pipes passed

Birds with higher scores are more likely to be selected for the next generation.
Configuration

The config_feedforward.txt file controls how NEAT behaves. Key parameters include:

    pop_size: Number of birds per generation.
    fitness_threshold: Score at which evolution ends.
    activation_default: Activation function (e.g., sigmoid).
    weight_mutate_rate: Mutation rate of connection weights.
    node_add_prob: Probability of adding new nodes.

Modify this file to experiment with different AI behaviors and learning speeds.
Running the Game

    Start the Game:

    python flappy_bird.py

    Watch the AI Learn: The game starts with a population of birds controlled by evolving neural networks. You’ll see generation numbers and scores on screen as the AI learns.

    Stop the Game: The game will end automatically if the fitness threshold is reached or can be closed manually.

Customization

    Game Assets: Replace images in the imgs/ directory to change the game's visual style.
    NEAT Settings: Tune values in config_feedforward.txt to control learning behavior.
