# Heap Sort
Third most popular sort (after quick and merge)
Always runs in n*log(n) time regardless of type of input

## Naive solution
Start with unsorted array
Heapify: convert array into heap

+ For each element in array insert it to the heap.
  + Heap insert logic will ensure result is a valid heap
+ After heap is built, extract every element.
  + Heap extract logic ensures we always extract min value (for minheap)
+ We build a new array by pushing every element we extracted.

### time complexity
n*log(n) for insertion
n*log(n) for extraction

### space complexity
2n for creating 2 arrays.

## Heap sort in place
We use the concept of a partition. Everything on one side is a valid heap, everything on the other side will be unsorted.

We will use a max heap here because it simplifies the process.

The first element in the heap will be automatically included.
Then we move the partition to include the second element.
Every element inserted into the heap has to maintain heap structure
When we're done we have a max heap.

Now we extract items right to left.
Rebuild the partition. Extracted elements go outside the partition. The heap goes on the other side.
When we extract all elements we are left with a fully sorted array.

### time complexity
n*log(n) for insertion
n*log(n) for extraction

### space complexity
O(1)

### advantages
- very stable, will always be n*log(n)
- in place
