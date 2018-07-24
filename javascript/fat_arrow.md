# Fat arrow functions
The fat arrow function is a more concise way of function expression

Several parameters
(param1, param2, ...  ,  paramN) => { //statements }

No Parameters
() => { statements }

## Syntax
If the function contains only the return statement we can leave out the return syntax

``let sayMyName = () => `Maya Shavin`
sayMyName() //"Maya Shavin"``

But if the return is an object literal we need to wrap it in parentheses

``let getObject2 = () => ({
  greet: function(){
    console.log('hi') }
    })

getObject2().greet() //hi``

If there's only one parameter we can omit the parentheses before the arrow

``let printName = name => console.log(name)``

## Binding 'this'
The value of ``this``  is determined by the outer scope in which the arrow function is used

## Takeaway
Arrow functions are syntactic sugar, there is little if any performance improvement. They are most useful for making more concise code and for intuitive handling of ``this``.
