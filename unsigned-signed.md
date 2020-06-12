## Bitwise Operator

- **#include <bitset>**
- Only works with unsigned int

` & ` : (bitwise AND) take two numbers as operands and does AND on every bit of two numbers. E.g. n&1 == 1 

` | ` : (bitwise OR)

`^` : (bitwise XOR)

` << ` : left shift: takes two numbers, left shifts the bits of the first operand, the second operand decides the number of places to shift 

` 0011 << 1 ` : is 0110

` 0011 << 2 ` : is 1100

` >> ` : right shift

` 1100 >> 1 `: is 0110

` ~ ` : bitwise NOT

Example of getting each bit from a number:
``` cpp
	Int n=100;
	for(int i=0;i<32;i++){
	Int bit=n&1;
	cout<<bit<<endl;
	n>>=1;
  }
```
Example of turn on a bit:
```cpp
	Int i,cin>>i;
	Int n=100;
	n=n|(1<<i);  // turn on 3th for example,  00000->00100
```
Example of turn off a bit:
```cpp
	Int i,cin>>i;
	Int n=100;
	n=n^(1<<i);  // turn on 3th for example,  00010->00000
```
