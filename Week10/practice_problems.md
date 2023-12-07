**Question 1** given a vector<int> in a function, return the function with all the elements in vector<int> in sorted order. There are no repeated/duplicate elements.
```
int main()
{
std::vector<int> vec={56,12,1,14,24,27,28,5,13};
get_sort(vec);
for(size_t i=0;i<vec.size();i++)
{
std::cout<<vec[i]<<" ";
}
std::cout<<std::endl;
return 0;
}
```
**Question 2** given a vec<int> in a function, return true if there are two elements present which add up to a certain number, example if 2+3 add up to 5 return true.
```
int main()
{
std::vector<int> vec={2,6,8,12,5,3,16};
bool flag=check(vec,5);
return 0;
}
```
**Question 3** Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once.
The relative order of the elements should be kept the same. Then return the number of unique elements in nums
```
int main()
{
std::vector<int> vec{1,1,1,1,4,4,4,6,6};
std::cout<<remove_dup(vec);//output is 3, vec is 1,4,6
return 0;
}
