# 🎬 Degrees of Separation in Hollywood 🎭

[![Python](https://img.shields.io/badge/Python-3.6+-blue.svg)](https://www.python.org/)
[![BFS Algorithm](https://img.shields.io/badge/Algorithm-BFS-green.svg)](https://en.wikipedia.org/wiki/Breadth-first_search)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🌐 Language / Idioma

-   🇺🇸 English (Current)
-   [🇪🇸 Español](README.es.md)

## 📝 Description

This project implements the famous **"Six Degrees of Separation"** concept (or "Six Degrees of Kevin Bacon") applied to the world of cinema. The application finds the shortest path connecting two actors through movies they have appeared in.

The theory suggests that any actor can be connected to Kevin Bacon (or any other actor) in six steps or fewer.

## 🚀 Features

-   🔍 Search by actor names
-   🧮 Implements a Breadth-First Search (BFS) algorithm
-   📊 Support for both small and large datasets
-   🎯 Name ambiguity resolution
-   📋 Displays the complete chain of connections between actors

## 🖼️ Example

![Execution example](images/console-example-01.png)

_The image shows an example of the program running where the connection between two actors is found._

## 🛠️ How It Works

The algorithm uses a graph data structure where:

-   **Nodes** are actors
-   **Edges** are movies in which two actors have worked together

To find the shortest connection, the program:

1. Loads actor and movie data from CSV files
2. Implements a Breadth-First Search (BFS) algorithm
3. Constructs and displays the shortest path between the two actors

## 📦 Data Structure

The program handles three main data structures:

-   `names`: Maps names to sets of person IDs
-   `people`: Maps person IDs to dictionaries with their name, birth year, and movies
-   `movies`: Maps movie IDs to dictionaries with title, year, and actors

## 💻 Usage

```bash
python degrees.py [directory]
```

Where `[directory]` is optional and can be:

-   `small` to use a reduced dataset (default)
-   `large` to use a complete dataset

## 🧩 Interaction Example

```
Loading data...
Data loaded.
Name: Emma Watson
Name: Kevin Bacon
2 degrees of separation.
1: Emma Watson and Actor X starred in Movie A
2: Actor X and Kevin Bacon starred in Movie B
```

## 🧠 Algorithm

The core of the project is the `shortest_path` function that implements a BFS algorithm to find the shortest path between two actors. This algorithm guarantees finding the path with the fewest connections.

## 📊 Datasets

-   **small**: A reduced set of actors and movies for quick testing
-   **large**: A more comprehensive database of the film world

## 🤝 Contributing

Contributions are welcome! You can improve the algorithm, optimize the code, or expand the database.

## 📜 License

This project is under the MIT License.

---

⭐ **Project inspired by the "Six Degrees of Kevin Bacon" concept** ⭐

---

<div align="center">
  <p>
    <small>Developed as part of <span style="font-weight: bold;">CS50's Introduction to Artificial Intelligence with Python</span> course on Edx - 2024</small>
  </p>
  <img src="https://img.shields.io/badge/Made%20with-Grid%20CSS-1572B6" alt="Made with: Nodes">
</div>
