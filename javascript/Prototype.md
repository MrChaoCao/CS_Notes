# Prototype
+ Objects default to having a prototype property with the value of object
+ The new operator sets the prototype property of the created object to whatever the created object is being created as a new instance of.
+ F.prototype is not the same as [[Prototype]]
+ F.prototype sets [[Prototype]] when new F() is called
+ F.prototype is always an object or null
+ prototype property only has special effect when it is set to a constructor function

[More resources](https://javascript.info/function-prototype)
