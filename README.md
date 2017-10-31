# Graphs

A C++ library for graph theory computations.

## Features
* Uses standard C++11 library.
* Constant time access to nodes and edges.
* Simple design and usage.

### Graph Theory Algorithms Included
* Breadth First Search Path Finding
* Tarjan's Strongly Connected Components Algorithm

## Installation
None required; simply dowload the library, then include it in your main.cpp

## Usage
### Creating Graphs

```c++
graph<int> newGraph; //Defines an empty graph with integer keys

newGraph.addVertex(1); //Define vertex with key 1
newGraph.addVertex(2); //Define vertex with key 2
newGraph.addVertex(3); //Define vertex with key 3

newGraph.addEdge(1,2); //Define edge connecting vertex 1 to vertex 2
newGraph.addEdge(1,3); //Define edge connecting vertex 1 to vertex 3
newGraph.addEdge(2,3); //Define edge connecting vertex 2 to vertex 3

newGraph.print();
```

Output will be:
```console
3 -> 
2 -> 3, 
1 -> 3, 2, 
```

### Creating Weighted Graphs

```c++
weighted_graph<int,double> newGraph; //Defines an empty graph with integer keys and double weights

newGraph.addVertex(1); //Define vertex with key 1
newGraph.addVertex(2); //Define vertex with key 2
newGraph.addVertex(3); //Define vertex with key 3

newGraph.addEdge(1,2,0.5); //Define edge connecting vertex 1 to vertex 2 with weight 0.5
newGraph.addEdge(1,3, 1.0); //Define edge connecting vertex 1 to vertex 3 with weight 0.5
newGraph.addEdge(2,3, 0.25); //Define edge connecting vertex 2 to vertex 3 with weight 0.5

newGraph.print();
```

Output will be:
```console
3 -> 
2 -> 3(0.25), 
1 -> 3(1), 2(0.5),
```
