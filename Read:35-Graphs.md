# Graphs

- A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.  
- Here is some common terminology used when working with Graphs:  

        - Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.  
        - Edge - An edge is a connection between two nodes.  
        - Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.  
        - Degree - The degree of a vertex is the number of edges connected to that vertex.  
## Directed vs Undirected
- is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.  

## Undirected
- The undirected graph we are looking at has 6 vertices and 7 undirected edges.  
- Vertices/Nodes = {a,b,c,d,e,f}  
- Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}  

![](./img/DirectedGraph.png)

## Directed
- The directed graph above has six vertices and eight directed edges  
- Vertices = {a,b,c,d,e,f}  
- Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}  

![](./img/DisconnectedGraph.png)

# Complete vs Connected vs Disconnected


## Complete Graphs
![](./img/CompleteGraph.png)

## Connected
![](./img/ConnectedGraph.png)

## Disconnected
![](./img/DisconnectedGraph.png)

## breath First Traversal 

```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)

    return nodes;
```

# Real World Uses of Graphs

- GPS and Mapping  
- Driving Directions  
- Social Networks  
- Airline Traffic  
- Netflix uses graphs for suggestions of products  
