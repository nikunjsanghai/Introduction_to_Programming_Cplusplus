**Question 1** given a vector<int> in a function, return the function with all the elements in vector<int> in sorted order. 
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
