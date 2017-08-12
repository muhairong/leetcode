# containers

A container is an object that stores other objects, which are all of a single type.

## some basic properties
- X::iterator compile time
- X::value_type compile time
- X u;  constant
- X();  constant
- X u(a); X u = a;  liner
- a.begin() a.end() constant
- a.size()  constant
- a.swap(b) constant
- a == b a != b liner
#### complexity
- compile time: during compilation and uses no excution time
- constant time: takes place during runtime but doesn't depend on the number of elements in an object
- liner time: is proportional to the number of elements

## Sequences
the elements are arranged in a definite order that doesn't change from one cycle of iteration to the next
### requiremens
