# Set

`begin()`
 - Returns an iterator to the first element in the set.

`end()` 
- Returns an iterator to the theoretical element that follows last element in the set.

`size()`
- Returns the number of elements in the set.

`max_size()`
- Returns the maximum number of elements that the set can hold.

`empty()` 
- Returns whether the set is empty.

```cpp
// empty set container
#include <set>
#include <iterator>
 
set <int, greater <int> > gquiz1;     
  
 // insert elements in random order
 gquiz1.insert(40);
 gquiz1.insert(50);
 gquiz1.insert(50); // only one 50 will be added to the set
 
 // printing set gquiz1
 set <int, greater <int> > :: iterator itr;
 for (itr = quiz 1.begin(); itr != gquiz1.end(); ++itr)
 {
     cout << '\t' << *itr;
 }
 cout << endl;
 
 // assigning the elements from gquiz1 to gquiz2
 set <int> gquiz2(gquiz1.begin(), gquiz1.end());
 
 // remove all elements up to 30 in gquiz2
 gquiz2.erase(gquiz2.begin(), gquiz2.find(30));
 
 // remove element with value 50 in gquiz2
 int num;
 num = gquiz2.erase (50);
 ```
