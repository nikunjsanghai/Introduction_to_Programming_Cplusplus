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

