# Object Relational Mapping (ORM)
ORM refers to converting data between incompatible type systems using object oriented programming languages.

## What is an object?
+ A phone book contains people. Each person can have multiple phone numbers and multiple addresses.
+ Person objects are modeled to have name, list of pone numbers, and a list of addresses
+ Phone number list would contain phone number objects
+ The address book is treated as a single object and various methods can be associated with the object.

## What is object relational mapping?
+ Many DBMS (such as SQL) can only store scalar values that are organized into tables
+ Programmer must convert object values into simpler groups of values that can be stored in the database
  + and convert them back upon retrieval


## Examples
+ Ruby
  + ActiveRecord
+ Python
  + Django
