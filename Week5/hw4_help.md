### Problem 1
Be very careful with the test case of 10, 10S,10D,10C,10H. I have seen multiple students type taking in account only 2 characters,
there is a case where this string will have 3 characters.Do take in account the four cases I have mentioned here. The output for the input:
```
10H
```
Output:
```
Ten of Hearts//check if your program gives this an output.
```
### Problem 2
While sorting your program should stop the moment you are able to determine if the character is larger or smaller. For example take the input:
```
aaabcc abbbaa acbaa
```
Step 1: Your program should be able to handle when the inputs are of different length. Read the question multiple times, a hint as to how to solve that is given already.       
Step 2: If your program does not stop when it is able to determine that aa is smaller than ab and ab is smaller is ac for the above input. It will continue to go on to
different characters. You would want to avoid that. Loop needs to break the moment you find order in characters/ or choose if statements suitably. 

### Problem 3
std::max(a,b) and std::min(a,b) were fairly useful in this question. 

### Problem 4
In this question your program should be able to handle both cases:         
Case1: Even number of elements in a vector       
Case2: Odd number of elements in a vector

