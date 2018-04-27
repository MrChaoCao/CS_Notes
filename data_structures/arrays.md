# Static Arrays
* Array implemented in C
* Fixed length, cannot change
* Methods Available
  + Get
  + Set

On declaration your application requests for a number of contiguous cells in memory

Each cell has a physical Address
Each cell holds 64 bits of information
Each cell is 8 bytes away from the last

On declaration we are told the the address of our first cell. Since we know the cell interval and the number of cells we need. We can find all of the cells in our array.

Any cell is at location: address + index * 8
Get and Set are constant operations. They just use the above formula.

Aside: 8 bytes = 64 Bits

## time complexity cheatsheet
  + find
    + O(1)
    + we know the start index, and the target index.
    + target is found at array[start + target index]
  + push
    + O(1)
    + Current size of array is tracked
    + New element is added at array[array.length]
  + delete
    + O(n)
    + Gaps in array need to be filled
    + All elements after the deleted element need to be shifted left

# Dynamic Arrays
When you create a new dynamic array you first create a new static array

capacity - the size of the initial static array being created

count - the number of items in our dynamic array

Methods
  push - add element / increment count
  pop - decrement count
  unshift
  shift

If we grow the array past the capacity we will need to make a new array
  copy the contents of the original array
  add the new element to an empty space
  we double the capacity every time we need to push
    amortized time complexity

Unshift and Shift
  Right now if we manipulate the beginning we throw off our whole count
  Shift - decrement count, increment starting address

  When we want to add elements to the front of the array there is no space
  So what we do is we add it to the end of the array and then we update the starting address

  With this re-organization of elements, it becomes hard to find the element at an index
    We solve this by taking the modulo of the index added to the start by the capacity
    new index = (start + index) % capacity

## time complexity of operations
  + push
    + O(1) amortized over n items

## time complexity of built in ruby array operations
  + inject
    + O(n) * times complexity of block passed in
  
