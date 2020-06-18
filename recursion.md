#Sample code

```cpp
int f(int n){
  /*base condition is really important to recursion, 
  otherwise recursion goes forever and throw overflow error*/
  
  if(n<=1)
    return 1;
  else
    return n*f(n-1);
```
- `Example`-Assume given n=3, 3*f(3-1)->3*f(2)->3*2*f(2-1)->3*2*f(1)=3*2*1=6
