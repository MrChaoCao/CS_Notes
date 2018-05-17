# Prototypal Inheritance
Every object has a private property
  This private property holds a link to another object: the prototype
  Every prototype also has a prototype
    The last prototype has a prototype of null
    null has no prototype
    null is the final link in the prototype chain

(Almost) All objects in JavaScript are instances of Object.
  Object is the top of the prototype chain

When trying to access the property of an object
  the property will be sought on the object
  and the objects prototype
  and the prototypes prototype
  until there end of the chain is reached or the property is found
