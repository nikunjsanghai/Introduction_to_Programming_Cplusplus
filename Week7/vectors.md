### Vectors 
Vectors are the same as dynamic arrays with the ability to resize itself automatically when an element is inserted or deleted, with their storage being handled automatically by the container. Vector elements are placed in contiguous storage so that they can be accessed and traversed using iterators. In vectors, data is inserted at the end. Inserting at the end takes differential time, as sometimes the array may need to be extended. Removing the last element takes only constant time because no resizing happens. Inserting and erasing at the beginning or in the middle is linear in time.

### std::vector in C++
std::vector in C++ is the class template that contains the vector container and its member functions. It is defined inside the /<vector/> header file. The member functions of std::vector class provide various functionalities to vector containers. Some commonly used member functions are written below:   

### Capacity
- size() – Returns the number of elements in the vector.
- max_size() – Returns the maximum number of elements that the vector can hold.
- capacity() – Returns the size of the storage space currently allocated to the vector expressed as number of elements.
- resize(n) – Resizes the container so that it contains ‘n’ elements.
- empty() – Returns whether the container is empty.
- shrink_to_fit() – Reduces the capacity of the container to fit its size and destroys all elements beyond the capacity.
- reserve() – Requests that the vector capacity be at least enough to contain n elements.

### Element Access
- reference operator [g] – Returns a reference to the element at position ‘g’ in the vector
- at(g) – Returns a reference to the element at position ‘g’ in the vector
- front() – Returns a reference to the first element in the vector
- back() – Returns a reference to the last element in the vector
- data() – Returns a direct pointer to the memory array used internally by the vector to store its owned elements.

### Modifiers
- assign() – It assigns new value to the vector elements by replacing old ones
- push_back() – It push the elements into a vector from the back
- pop_back() – It is used to pop or remove elements from a vector from the back.
- insert() – It inserts new elements before the element at the specified position
- erase() – It is used to remove elements from a container from the specified position or range.
- swap() – It is used to swap the contents of one vector with another vector of same type. Sizes may differ.
- clear() – It is used to remove all the elements of the vector container
- emplace() – It extends the container by inserting new element at position
- emplace_back() – It is used to insert a new element into the vector container, the new element is added to the end of the vector


### Vector Thoery
Vectors are sequence containers representing arrays that can change in size.                                

Just like arrays, vectors use contiguous storage locations for their elements, which means that their elements can also be accessed using offsets on regular pointers
to its elements, and just as efficiently as in arrays. But unlike arrays, their size can change dynamically, with their storage being handled automatically by the 
container.                          

Internally, vectors use a dynamically allocated array to store their elements.                               
This array may need to be reallocated in order to grow in size when new elements are inserted, which implies allocating a new array and moving all elements to it.
This is a relatively expensive task in terms of processing time, and thus, vectors do not reallocate each time an element is added to the container.                     

Instead, vector containers may allocate some extra storage to accommodate for possible growth,
and thus the container may have an actual capacity greater than the storage strictly needed to contain its elements (i.e., its size).
Libraries can implement different strategies for growth to balance between memory usage and reallocations, but in any case,
reallocations should only happen at logarithmically growing intervals of size so that the insertion of individual elements at the end of the vector can be provided
with amortized constant time complexity (see push_back).                          

Therefore, compared to arrays, vectors consume more memory in exchange for the ability to manage storage and grow dynamically in an efficient way.                 

Compared to the other dynamic sequence containers (deques, lists and forward_lists), vectors are very efficient accessing its elements (just like arrays) and relatively efficient adding or removing elements from its end. For operations that involve inserting or removing elements at positions other than the end,
they perform worse than the others, and have less consistent iterators and references than lists and forward_lists.        


Reference Link: [geeksforgeeks](https://www.geeksforgeeks.org/vectorempty-vectorsize-c-stl/) [geeksforgeeks](https://www.geeksforgeeks.org/vector-in-cpp-stl/) [geeksforgeeks](https://www.geeksforgeeks.org/vector-resize-c-stl/) [geeksforgeeks](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/) [cppref](https://en.cppreference.com/w/cpp/container/vector) [cplusplus](https://cplusplus.com/reference/vector/vector/) [geeksforgeeks](
https://www.geeksforgeeks.org/vector-in-cpp-stl/#)
