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
