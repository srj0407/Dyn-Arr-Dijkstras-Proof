# Dyn-Arr-Dijkstras-Proof

# Priority Queue and Dijkstra's Algorithm

This repository contains implementations and utilities for working with priority queues and solving graph problems using Dijkstra's algorithm. It includes modular C code for handling dynamic arrays, priority queues, and a test driver for verifying functionality.

## Files Overview

### Core Implementation
- **`dijkstra.c`**:
  - Implementation of Dijkstra's algorithm to find the shortest paths in a graph defined in `airports.dat`.
  - Reads graph data from the file and calculates the least-cost paths.

- **`pq.c`** and **`pq.h`**:
  - A priority queue implementation where lower numerical priority corresponds to higher logical priority.
  - Includes core functions like `pq_create`, `pq_insert`, and `pq_remove_first`.

- **`dynarray.c`** and **`dynarray.h`**:
  - A dynamic array implementation used as a building block for the priority queue.
  - Includes functionality to resize dynamically, insert, remove, and access elements.

### Data Files
- **`airports.dat`**:
  - A data file representing a graph in terms of nodes (airports) and edges (connections).
  - Format: The first two integers specify the number of nodes and edges, followed by edges with weights.

### Testing and Utilities
- **`test_pq.c`**:
  - A test suite for the priority queue implementation.
  - Inserts and removes elements while validating the correctness of the priority-based operations.

- **`Makefile`**:
  - Simplifies compilation of the project. Contains targets for building the main program, test files, and cleaning up.

## Compilation and Usage

1. **Compilation**:
   Use the `Makefile` for building the project. Run the following commands:
   ```bash
   make
   ```
   This will generate the executable files.

2. **Running Dijkstra's Algorithm**:
   Execute the main program to calculate shortest paths:
   ```bash
   ./dijkstra
   ```

3. **Testing the Priority Queue**:
   Run the test suite:
   ```bash
   ./test_pq
   ```

4. **Cleaning Up**:
   To remove compiled files, run:
   ```bash
   make clean
   ```

## Project Structure

- **Dynamic Arrays**: Serve as the foundation for the priority queue.
- **Priority Queue**: Implements a robust structure for managing elements based on their priority.
- **Dijkstra's Algorithm**: Uses the priority queue to compute shortest paths efficiently.

## Future Enhancements

- Extend the priority queue to support custom comparison functions.
- Optimize the Dijkstra implementation for sparse graphs using a Fibonacci heap.
- Add more comprehensive tests for edge cases in `test_pq.c`.
