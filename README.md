# simulation-autonomous-forklift

## Introduction

This Python script provides a tool for simulating the behavior of forklifts in a manufacturing setting. It's particularly helpful for predicting possible collisions based on forklifts' movement paths, speeds, waiting times, and acceleration, allowing for better planning and optimization of the operations.

## Dependencies

This code requires the following Python libraries:

- `numpy`
- `math`
- `matplotlib`
- `pandas`
- `itertools`

## Code Overview

The Python script consists of the following parts:

1. **Calculate the coordinates of the individual stations:** This section of the script involves defining functions for calculating the x, y coordinates of the stations based on distances and angles between stations. The calculated coordinates are visualized using matplotlib.

2. **Define forklift class:** The Forklift class simulates a forklift moving along a route, considering its acceleration. The forklift moves along a defined route, waits for a defined period at each station, and accelerates from zero to a defined maximum speed.

3. **Forklift Simulation Function:** This function simulates the movement of multiple forklifts along their routes for a specified amount of time. It checks for collisions by comparing the distance between all pairs of forklifts to a specified safety distance.

4. **Grid Creation and Simulation:** This section of the script creates a grid of all possible speed combinations for the forklifts. The forklifts are simulated with each speed combination, and the simulation result is added to a DataFrame. Finally, the speed combinations that did not lead to a collision are identified, and the combination with the maximum combined speed is printed.

## Usage

Run the python script to visualize the calculated positions of the stations and the routes of the forklifts. Then, the simulation runs with all the combinations of speeds for the forklifts. 

The script prints out the combinations of speeds that did not result in any collisions within a 24-hour simulation, and it also identifies the fastest speed combination that did not result in a collision.
