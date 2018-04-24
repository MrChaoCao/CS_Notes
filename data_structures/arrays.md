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
