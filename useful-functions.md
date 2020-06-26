# Some useful functions in C++

### swap(a, b): 
`swap(nums[i], nums[j]);`

### sort():
`sort(vector1.begin(), vector1.end())`

### for loop:
```cpp
for (auto&& [first,second] : mymap) {
    // use first and second
}
```
```cpp
for (auto i : v) // access by value, v is a vector, i is v[index]
  std::cout << i << ' ';
```

### if-statement:
`z = (x > y) ? z : y;`

is equivalent to 
```cpp
if (x > y) {
  z = z;
} 
else {
  z = y;
}
```
