# containers

A container is an object that stores other objects, which are all of a single type.

## some basic properties
- X::iterator | compile time
- X::value_type | compile time
- X u;  | constant
- X();  | constant
- X u(a); X u = a;  | liner
- a.begin() a.end() | constant
- a.size()  | constant
- a.swap(b) | constant
- a == b a != b | liner
#### complexity
- compile time: during compilation and uses no excution time
- constant time: takes place during runtime but doesn't depend on the number of elements in an object
- liner time: is proportional to the number of elements

## Sequences
the elements are arranged in a definite order that doesn't change from one cycle of iteration to the next
#### requiremens
- a.insert(p, t)  a.insert(p, n, t) a.insert(p, i, j) | insert... before p
- a.erase(p)  a.erase(p, q)
- a.clear()
they have constant-time complexity
#### optional requirements
- a.front() a.back()
- a.push_back(t) a.pop_back(t)
- a.push_front(t) a.pop_front(t)
- a[n] a.at(n)

### vector
1. vector is a class representation of an arry
2. provides automatic memory management that allows the size of a vector object to vary dynamically, growing and shrinking as elements are add or removed
3. provides random access to elements
4. elements can be added to or removed from the end in constant time, but insertion and removal from the beginning and the middle are linear-time operations
5. reversible container: rbegin(), rend()

### deque
1. represents a double-ended queue
2. supporting random access
3. inserting and removing items from the beginning of a deque object are constant-time operations

### list
1. provides for constant-time insertion and removal of elements at any location in the list
2. vector emphasizes rapid access via ramdom access, whereas list emphasizes rapid insertion and removal of elements
3. reversible
4. does not support array natation and random access
5. some lisr member funtions
  * void merge(x) list must be sortes, and x is left empty
  * void remove(val) removes all instances of val from the list
  * void sort() complexity is nlogn
  * void splice(pos, x) inserts the contents of list x in front of position pos, and x is left empty
  * void unique() only reduces adjacent equal values to a single value

### queue
1. allows an underlying class(deque, by default) to exhibit the typical queue interface
2. add an element to the rear of a queue, remove an element from the front of a queue, view the values of the front and rear elements, check the number of elements, and test to see if a queue is empty
3. empty(), size(), front(), back(), push(x), pop()

### priority_queue
1. supports the same operations as queue
2. the largest item gets moved to the front of the queue

### stack
1. push a value onto the top of a stack, pop an element from the pop of a stack, view the values at the top of a stack, check the number of elements, and test wheter the stack is empty
2. empty(), size(), top(), push(x), pop()
