# Types
Loom's type system is based around two categories: **reference types** and **value types**.


## Value Types
Value Types (`structs`) contain data directly. Movement of a value type creates an independent copy of its data.
```loom
i32 valueType = 10;
i32 copy = valueType;

copy = 20;

printf(valueType); // 10
printf(copy); // 20
```


## Reference Types 
Reference Types (`classes`) contain a pointer to data. Movement of a reference type is governed by Loom's smart-pointer model.

### Unique Pointers
Unique Pointers provide exclusive ownership of an object. Moving a unique pointer to another unique pointer transfers ownership, invalidating the original. This allows compile-time memory validation with no extra performance impact.
```loom
unique string myString = "Hello, World!";
unique string passed = myString;

printf(myString); // Compile Error, myString is not owner!
printf(passed); // "Hello, World!"
```

### Shared Pointers
Shared Pointers provide shared ownership of an object. Moving a shared pointer to another shared pointer increments an internal instance counter, allowing both the original and the current to be used.
```loom
shared string myString = "Hello, World!";
shared string passed = myString;

printf(myString); // "Hello, World!"
printf(passed); // "Hello, World!"
```
