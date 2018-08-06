# Graph Implementation
G = (V, E)

To build a graph, create a list to store all vertices and a list to store all edges.

Vertex list would be a simple list of the vertices we have

Edges are defined by their 2 endpoints. We can make an object to represent edges by their start and end vertices. The edges list would be a list of tuples

For weighted graphs we can have a 3-tuple with start vertex, end vertex, and weight.

Space complexity of a graph is proportional to the number of edges in the graph.
  vertex list: O(|V|)
  edge list: O(|E|)
  graph: O(|V| + |E|)

As an improvement. Rather than keeping a list of vertices and an edge list maintaining a copy of the vertex list with any associated weight. We can build an Edge list with references to vertices in the vertex list.


Frequently performed operations
  + Finding all adjacent nodes to a given node.
    + O(|E|). We must search all edges to see what edges connect to the given node.
  + Determining if two edges are connected.
    + O(|E|). We must search all edges to see what edges connect to the given node.

Recalling
0 <= |E| <= V(V-1) if directed or V(V-1) / 2 if undirected

Time cost is inefficient if the time complexity scales with |E|. 
