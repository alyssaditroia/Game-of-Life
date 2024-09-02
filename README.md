# Conway's Game of Life

## Description

This project is a basic implementation of Conway's Game of Life in C. The program simulates the evolution of a 10x10 grid of cells based on specific rules. Each cell can either be alive or dead, and its state in the next generation depends on the number of live neighbors it has.

## Features

- **Grid Size:** 10x10 grid.
- **Generation Count:** Up to 40 generations are simulated.
- **User Input:** The user provides 20 numbers to initialize the grid's live cells.
- **Visualization:** The grid is printed to the console, with live cells represented by `*` and dead cells by `.`.

## How to Play

1. **Start the Program:** 
   - Run the program, and you will be welcomed to the Game of Life.
   - Enter any key to start or `q` to quit.

2. **Initialize the Grid:**
   - You will be prompted to enter 20 numbers from 2 to 101, separated by commas.
   - These numbers correspond to specific cells on the grid, which will be set as alive.

3. **Observe Generations:**
   - The program will simulate up to 40 generations, updating the grid based on the Game of Life rules.
   - The grid is displayed after each generation.

4. **End of the Game:**
   - The game ends if all cells are dead or if 40 generations are reached.

## Rules of the Game

- A live cell with fewer than two live neighbors dies (underpopulation).
- A live cell with two or three live neighbors lives on to the next generation.
- A live cell with more than three live neighbors dies (overpopulation).
- A dead cell with exactly three live neighbors becomes a live cell (reproduction).

## Code Overview

- **Main Functions:**
  - `playGameOfLife()`: Manages the game loop and user interaction.
  - `getPlayerGrid()`: Initializes the grid based on user input.
  - `determineNeighbors()`: Counts live neighbors for a given cell.
  - `neighborCountGrid()`: Creates a grid of neighbor counts.
  - `generationLogic()`: Applies the Game of Life rules to update the grid.
  - `hasLiveCells()`: Checks if any live cells remain on the grid.
  - `printGrid()`: Prints the grid to the console.

## Requirements

- **C Compiler:** Any standard C compiler (e.g., GCC).
- **Operating System:** Linux, macOS, or any system that supports `system("clear")` for screen clearing.

## How to Compile and Run

1. **Compile:**
   ```sh
   gcc -o life life.c

