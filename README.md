# Degrees Project

## Project Overview

The Degrees Project is designed to find the shortest path between two actors through their filmography. This project uses a graph-based approach to determine the degrees of separation between actors, similar to the concept of "Six Degrees of Kevin Bacon."

## Functionality

- **Input**: The user provides the names of two actors.
- **Output**: The program outputs the shortest path of movies and co-actors that connect the two actors.
- **Data Source**: The project uses a dataset containing information about actors and the movies they have appeared in.

## Type of Search

The project implements two types of search algorithms to explore the graph of actors and movies:

### Breadth-First Search (BFS)

BFS is chosen because it efficiently finds the shortest path in an unweighted graph.

- **Initialization**: Start from the source actor and initialize a queue.
- **Exploration**: Dequeue an actor, explore all connected actors through movies, and enqueue them if they haven't been visited.
- **Termination**: The search terminates when the target actor is found or all possible connections have been explored.

### Steps of BFS

1. Enqueue the starting actor.
2. Dequeue an actor and mark it as visited.
3. For each movie the actor has appeared in, enqueue all co-actors who haven't been visited.
4. Repeat until the target actor is found or the queue is empty.

### Depth-First Search (DFS)

DFS is another search algorithm that explores as far as possible along each branch before backtracking.

- **Initialization**: Start from the source actor and initialize a stack.
- **Exploration**: Pop an actor from the stack, explore all connected actors through movies, and push them onto the stack if they haven't been visited.
- **Termination**: The search terminates when the target actor is found or all possible connections have been explored.

### Steps of DFS

1. Push the starting actor onto the stack.
2. Pop an actor from the stack and mark it as visited.
3. For each movie the actor has appeared in, push all co-actors who haven't been visited onto the stack.
4. Repeat until the target actor is found or the stack is empty.

## Example

If the user inputs "Leonardo DiCaprio" and "Tom Hanks," the program will output the shortest path of movies and co-actors connecting these two actors.

## Usage

### Cloning the Project

To clone the project, run the following command in your terminal:

```sh
git clone https://github.com/sandovaldavid/project0_degrees.git
```

### Running the Project

1. Navigate to the project directory:

```sh
cd degrees
```

2. Choose the dataset directory (small or large):

```sh
python degrees.py [dataset_directory]
```

Replace `[dataset_directory]` with either `small` or `large` depending on the dataset you want to use.

- For the small dataset:

```sh
python degrees.py small
```

- For the large dataset:

```sh
python degrees.py large
```

3. Follow the prompts to input the names of the two actors you want to connect.

### Example Output

```bash
Actor 1: Leonardo DiCaprio
Actor 2: Tom Hanks
1 degree(s) of separation.
1: Leonardo DiCaprio and Tom Hanks starred in Catch Me If You Can
```

## Conclusion

The Degrees Project demonstrates the application of graph theory and search algorithms in solving real-world problems related to network connections and shortest paths.
