 # erase()
 
- `erase()` is used to erase the pair in map mentioned in argument, either its position, its value or a range of number.

- `erase(key)` : Erases the key-value pair using key mentioned in its argument. reorders the map after deletion. 
It returns the number of entries deleted. If non-existing keys is deleted, 0 is returned.
  - Time complexity : log(n) (n is size of map)

- `erase(iter)` : Erases the pair at the position pointed by the iterator mentioned in its argument.
  - Time complexity : log(n) (n is size of map)

- `erase(strt_iter, end_iter)` : Erases the range of pairs starting from “strt_iter” to the “end_iter”.
  - Time complexity : O(k) (k is size of map)
