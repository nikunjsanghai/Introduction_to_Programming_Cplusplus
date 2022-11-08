### Vectors 
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


### Functions in std::vector 

#### Size
Returns the number of elements in the vector.
```
#include <bits/stdc++.h>
using namespace std;

int main()
{

	// Initializing a vector of string type
	vector<string> vec = { "Geeks", "For", "Geeks" };

	for (int i = 0 ; i <= vec.size() - 1 ; i++)
		cout << vec[i] << ' ';
	return 0;
}
```
Output:
```
Geeks For Geeks 
```
#### resize 
Resizes the container so that it contains ‘n’ elements. Syntax:
```
vectorname.resize(int n, int val)
```
Output:
```
Parameters:

n – it is new container size, expressed in number of elements.
val – if this parameter is specified then new elements are initialized with this value.
Return value:

This function do not returns anything.
Exception:

The only exception if it so happens is Bad_alloc thrown, if reallocation fails.
```

Reference Link: [geeksforgeeks](https://www.geeksforgeeks.org/vectorempty-vectorsize-c-stl/) [geeksforgeeks](https://www.geeksforgeeks.org/vector-in-cpp-stl/) [geeksforgeeks](https://www.geeksforgeeks.org/vector-resize-c-stl/) [geeksforgeeks](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/) [cppref](https://en.cppreference.com/w/cpp/container/vector) [cplusplus](https://cplusplus.com/reference/vector/vector/)
