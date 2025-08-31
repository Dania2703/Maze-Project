# Maze Project – Generation, Search, and Server Communication

This project implements a complete framework for working with mazes, including **maze generation algorithms**, **search algorithms**, **compression utilities**, and **client-server communication** for solving maze problems. It is written in Java and organized into multiple packages for modularity.

## Features
### Maze Generation (`algorithms.mazeGenerators`)
- `EmptyMazeGenerator` – generates an empty maze
- `SimpleMazeGenerator` – generates simple mazes
- `MyMazeGenerator` – generates more complex mazes
- `Maze`, `Position` – data structures for maze representation

### Search Algorithms (`algorithms.search`)
- `DepthFirstSearch`
- `BreadthFirstSearch`
- `BestFirstSearch`
- Unified search interfaces (`ISearchable`, `ISearchingAlgorithm`) and state representations (`AState`, `MazeState`, `Solution`)

### Compression and Decompression (`IO`)
- Custom compressor and decompressor classes to efficiently store and load mazes

### Server and Client (`Server`, `Client`)
- `Server` and `Client` classes enable distributed solving of maze problems
- Strategies:
  - `ServerStrategyGenerateMaze` – generates mazes on demand
  - `ServerStrategySolveSearchProblem` – solves search problems remotely

### Testing (`test`)
- Utilities to validate:
  - Maze generation
  - Compression/decompression
  - Search algorithms
  - Client-server communication

## How to Run
1. Compile all Java files inside the `src` directory using  
   javac src/**/*.java  
2. Run the server and then execute client test classes to interact with it:  
   java Server.Server  
   java test.RunMazeGenerator  
   java test.RunSearchOnMaze  
   java test.RunCommunicateWithServers  
   java test.RunCompressDecompressMaze  

## Final Result
- **Maze generation** produces mazes of different complexity levels  
- **Search algorithms** find paths through mazes using DFS, BFS, or Best-First Search, returning solution paths and steps count  
- **Compression utilities** allow mazes to be saved and restored efficiently  
- **Server communication** enables clients to request mazes or solutions from a server, simulating distributed AI problem-solving  

## Requirements
- Java 8 or later

## Applications
- Understanding search algorithms in AI  
- Demonstrating client-server communication in Java  
- Practicing modular programming with packages  
- Teaching maze generation, search heuristics, and data compression  

## License
MIT (free to use and modify)
