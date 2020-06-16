## Unordered Map

**Unordered_map is an associated container that stores elements formed by combination of key value and a mapped value. 
The key value is used to uniquely identify the element and mapped value is the content associated with the key.
Both key and value can be of any type predefined or user-defined.**

```cpp
#include<unordered_map>
unordered_map<string, int> umap;
umap[“A”] = 10;
for(auto x : umap)
cout << x.first << “ “ << x.second << endl;
 
std::unordered_map<std::string,double> mymap = {
     {"mom",5.4},
     {"dad",6.1},
     {"bro",5.9} };
 
std::unordered_map<std::string,double>::const_iterator got = mymap.find (x); // finding x 
  if ( got == mymap.end() )
    std::cout << "not found";
  else
    std::cout << got->first << " is " << got->second;
 
erase() :
it=mymap.find('b');
  mymap.erase (it);                   // erasing by iterator


  mymap.erase ('c');                  // erasing by key


  it=mymap.find ('e');
  mymap.erase ( it, mymap.end() );    // erasing by range
insert()
std::unordered_map<std::string,double>
              myrecipe,
              mypantry = {{"milk",2.0},{"flour",1.5}};


  std::pair<std::string,double> myshopping ("baking powder",0.3);


  myrecipe.insert (myshopping);                        // copy insertion
  myrecipe.insert (std::make_pair<std::string,double>("eggs",6.0)); // move insertion
  myrecipe.insert (mypantry.begin(), mypantry.end());  // range insertion
  myrecipe.insert ( {{"sugar",0.8},{"salt",0.1}} );    // initializer list insertion
  ```
