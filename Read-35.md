# **Graphs**

## **What is Graphs ?**

* A graph is a non-linear data structure
* can be looked at as a collection of vertices
* connected by line segments named edges.

## **Terminology**

* `Vertex`: also called a “node”, is a data object that can have zero or more adjacent vertices.
* `Edge`: is a connection between two nodes.
* `Neighbor`: The neighbors of a node are its adjacent nodes
* `Degree`: The degree of a vertex is the number of edges connected to that vertex.

## **Directed vs Undirected**

### **Undirected Graphs**

graph where each edge is undirected or bi-directional.

![Undirected](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

### **Directed Graphs (Digraph)**

graph where every edge is directed.

![Directed](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

## **Complete vs Connected vs Disconnected**

### **Complete Graphs:**

A Complete graph is a simple undirected graph in which every pair of distinct vertices is connected by a unique edge.

![Complete](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/CompleteGraph.PNG)

### **Connected Graphs:**

It is a graph in which each node has at least one edge.

![Connected](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/ConnectedGraph.PNG)

### **Disconnected Graphs:**

It is a graph in which some node may not have edges.

![Disconnected](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DisconnectedGraph.PNG)

## **Acyclic vs Cyclic**

### **Acyclic Graph:**

An acyclic graph is a directed graph without cycles.

![Acyclic](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/threeAcyclic.png)

### **Cyclic Graph:**

A Cyclic graph is a graph that has cycles.

![Cyclic](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/cyclic.PNG)

## **Graph Representation**

* **Adjacency Matrix:**

  * Is represented through a 2-dimensional array.

* **Adjacency List:**

  * The most common way to represent graphs.
  * An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

## **Weighted Graph?**

It is a graph with graph numbers assigned to its edges.

![Weighted Graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightGraph.PNG)

By using a weight you can make calculation to find the better path, by calculation the total sum of the edges in each path.

## **Traversals:**

We can use either use `Breadth First` or `Depth First` in travelling in the graph.

### **Depth First:**

![Depth First](https://i.stack.imgur.com/QnStc.png)

### **Breadth First:**

![Breadth First](https://i.ytimg.com/vi/QRq6p9s8NVg/maxresdefault.jpg)

## **Real World Uses of Graphs**

* GPS and Mapping
* Driving Directions
* Social Networks
* Airline Traffic
* Netflix uses graphs for suggestions of products


[HOME](https://malkhaleel88.github.io/reading-notes)