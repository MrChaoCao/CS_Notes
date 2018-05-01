# Priority Queue
Concept:
Queue is implemented with tiers of priority
Elements in queue are ranked by priority, not seniority

## Linked List approach
+ Give each node a priority property
+ Naive solution - iterate through list until we find the end of our priority tier
+ Better solution - pointers to the start of each prioritiy tier
+ With unlimited tiers of priority this becomes impractical

## Array approach
+ build array of all elements then sort based on priority tier
+ even worse because sorting is nlogn time

## Heap
Ideal datastructure for implementing a Priority Queue
used for Heap sort
specialty: can access minimum and maximum values in constant time

### 3 methods:
  1. peek: constant time
  2. insert: better than linear time
  3. extract: better than linear time

### Heaps are Binary tree that follows certain constraints
  + each node has at most 2 children
  + full: all non-leaf nodes have exactly 2 children
  + complete: tree is populated top to bottom left to right
    + doesn't need to be full
  + heaps must be complete trees
  + heaps must obey heap properties (min vs max)
    + MinHeap Parent nodes must be smaller than all of their children
    + MaxHeap Parents nodes must be larger than all of their children

#### Peek
  O(1) runtime, sees smallest item (at top of tree)

#### Insert
  If inserted value disobeys heap property
    swap value with its parent and continue until it obeys the heap property
  Heapify up:
    swapping values with their parents until the heap is properly sorted
  Time complexity:
    O(log(n)) - we swap a number of times proportional to the depth of the child node

#### Extract
Extracting is a little tricky. If we remove our root node, the rules of inheritance are difficult to implement. When the root is gone, which child should become the new root, then how would we resolve the rest of the tree structure.

When we want to extract the root, we switch it with the only leaf whose removal allows the heap to continue obeying the heap property. Now very large element is at the top of our min heap. This is easy to solve we heapify down.

Heapify down:
  Root swaps with its smallest child (left if they're equivalent)
  Continue swapping until we have no chilren, or root is larger than children
  time complexity: O(log(n))
