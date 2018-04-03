# Call stack
Data structure that records where in the program we are
push on the top, pop off the top

example

function multiply (a, b){
  return a * b;
}
function square(n) {
  return multiply(n, n);
}
function printSquare(n) {
  var squared = square(n);
  console.log(squared);
}
printSquare(4);

Stack:

multiply(n, n)
square(n)
printSquare(4)
main()

pop things off the top until we finish call stack.

# blocking what happens when things are slow.
When we're single threaded and synchronous, nothing can execute while the stack is active. Computer needs to finish what its doing before it can take new input. Can't even show user that it is processing requests -> user frustration.

# asynchronous callbacks
How do these interact with the stack?
When using set time out, the asynchronous callback is pushed to the stack, then resolved, then the next item is pushed to the stack and resolves. After the timer has finished, the asynchronous callback comes back.

# concurrency and the event loop
When asynchronous callbacks are pushed onto the stack they will run in the background while the stack is processed as normal. When the asynch call is done it gets pushed onto the task queue. If the asynch call was pushed on the stack immediately it would cause havoc, callbacks would be taking place in the middle of other code.

The task queue pushes items onto the stack when the stack is empty.
Set time out is not a guaranteed time until execution. It is a minimum time, after the timeout it will be pushed onto the callback queue and will execute when the stack is emptied. For example set timeout 0 will execute whenever the stack is empty.

Don't block he event loop. For any slow to run code you have, make it asynchronous so that the browser can update and provide the user with a responsive experience.
