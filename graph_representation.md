# Adjacency matrix
+ Square matrix
+ N**2 space consumption, N is number of vertices
+ row index is start point, col index is end point
+ index is start point, value is the presence of an edge

+ we wind up storing both the presence of an edge, and its absence
+ for sparse graphs we wind up with a thousand times more empty connections than edges

+ index represents nothing
+ value represents the connection
+ Binary search tree instead of an array
+ space consumption O(e) where e is edges
  + usually e << v**2

## Time cost of operations
+ Determining if 2 nodes are connected
  + Adjacency matrix: constant. A[start][end]
  + Adjacency list: must iterate through the row
    + linear search: O(v), O(logv) if binary search
+ Finding all neighbors of a node.
  + O(v) for both methods
  + however average case is dramatically improved for a sparse graph
+ Insertion of a new edge
  + Adjacency matrix, O(1), just update that specific cell
  + Adjacency list, O(1)

  Adjacency list:
  unweighted, undirected: nodes have value and pointer to the next node in list
  Weighted: node has value, pointer, and edge weight

  Space: |E| + |v|
