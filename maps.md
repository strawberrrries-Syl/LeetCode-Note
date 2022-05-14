## 1. init
```cpp
map<key, value> name;
```
## 2.  insert
```cpp
map[key];
```

## 3. find
```cpp
map.find(key)
```
if key does not exist, return map.end()

## 4. hash map:

```cpp
unordered_map<key, value> name;

map.find(key) != map.end(); // key exist
// if want to get value from find function
map.find(key)->first; // aim key
map.find(key)->second; // aim value

map.insert(pair <string, double> (key, value));
// or
map.insert({key, value});


// iter:
for(itertor iter = map.begin(); iter != map.end(); iter++)
{ 
  cout<< "key value: " << iter->first << "value: " << iter->second << endl;
}
// or:
for(auto& v:map)
{
  cout << v.first << v.second
}

map.empty(); // empty-> return true, have element ->return false



```
