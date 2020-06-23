# Stringstream

#### [Declaration]:
```cpp
#include <sstream>  
stringstream ss;
```
#### [How to use it?]
```cpp
/* stringstream supports input operation: inserts data into the stream.*/
ss << 100 << ' ' << 200;

int foo,bar;
/* stringstream supports output operation: extracts data out of a string stream*/
ss >> foo >> bar;  // foo = 100, bar == 200
```

```cpp
/* returns a string object with a copy of the current contents of the stream*/
std::string s = ss.str();
```

```cpp
string str = "Hello Hello Hello";
stringstream str_strm(str);  // convert string to a string stream
string tmp;
while (str_strm >> tmp) {   
    ...
}
```
```cpp
/* To get and set the string object whose content is present in stream*/
string res = my_ss.str();
```

### istringstream
```cpp
/* Convert a list of integers in string to ints*/
std::string stringvalues = "125 320 512 750 333";
std::istringstream iss (stringvalues);
int val;
while(iss >> val){
  ...
}
```

```cpp
istringstream stream1;
string string1 = "25";
stream1.str(string1);
```
