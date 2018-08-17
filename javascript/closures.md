## Execution context.
global code: default environment where your code is first executed
function code: whenever the flow of execution enters a function body

When a function is called
  + a new, local execution context is created
  + the local execution context has its own variables
  + new execution context is added to the execution stack
    + execution stack keeps track of where the program is in execution

A function ends at a return statement or a closing bracket }
  + the local execution context pops of the execution stack
  + the function sends its return to the calling context.
  + the local execution context is destroyed, local variables are erased

```
1: let a = 3
2: function addTwo(x) {
3:   let ret = x + 2
4:   return ret
5: }
6: let b = addTwo(a)
7: console.log(b)
```

The variable a is defined in the global execution environment
The function addTwo is defined in the global execution environment

When b is declared on line 6 and addTwo is invoked we
  instantiate the local execution environment of addTwo
  the value of 3 is passed in to addTwo
    x is assigned the value of 3
    the variable ret is declared in addTwo
    ret is calculated and returned
  the local execution environment of addTwo is destroyed only keeping 5

## Lexical scope
