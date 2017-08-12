# iterator

iterator is a generalization of a pointer. 
- pointer
- object

allows STL to provide a uniform interface for a variety of container classes
makes the algotithms independent of the type of container used

vector<double>::iterator pd;

STL defines five kinds of iterators: input iterator, output iterator, forward iterator, bidirectional iterator and random access iterator.

## pointer as iterator
STL algorithms can use pointer to operate on non-STL containers that are based on pointers
eg.
```
const int SIZE = 100;
double Receipts[SIZE];
//use STL sort() function
//first element: &Receipts[0] or just Receipts
//one-past-the-end: &Receipts[SIZE] or just Receipts + SIZE
sort(Receipts, Receipts + SIZE);
```

## copy(), ostream_iterator, and istream_iterator
- copy(casts, casts + 10, dice.begin()); //copy the array to vector
- ostream_iterator<int, char> out_iter(cout, " ") //*out_iter++ = 15;
- copy(dice.begin(), dice.end(), out_iter);
- copy(istream_iterator<int, char>(cin), istream_iterator<int, char>(), dice.begin());

## other useful iterators
### reverse_iterator, back_insert_iterator, front_insert_iterator, and insert_iterator
1. reverse_iterator
	1. rbegin(), rend()
	2. copy(dice.rbegin(), dice.rend(), out_iter); // display in reverse order
	3. rp is a reverse pointer, *rp dereferences the iterator value immediately preceding the current value of *rp
2. back_insert_iterator, front_insert_iterator, and insert_iterator
	1. insertion adds new elements without overwriting existing data, and it uses automatic memory allocation to ensure that the new information fits
	2. back_insert_iterator inserts items at the end of the container
	3. front_insert_iterator inserts items at the front
	4. insert_iterator inserts items in front of the location specified as an argument to the insert_iterator constructor.
3. back_insert_iterator<vector<int>> back_iter(dice); // a back_insert_iterator for a vector<int> container called dice
4. insert_iterator<vector<int>> insert_iter(dice, dice.begin());
