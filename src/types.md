# Types
Loom's type system is based around two categories: **reference types** and **value types**.


## Value Types
Value Types (`structs`) contain data directly. Movement of a value type creates an independent copy of its data.
```loom
i32 valueType = 10;
i32 copy = valueType;

copy = 20;

println(valueType); // 10
println(copy); // 20
```


## Reference Types 
Reference Types (`classes`) contain a pointer to data. Movement of a reference type is governed by Loom's smart-pointer model.

### Unique Pointers
Unique Pointers provide exclusive ownership of an object. Moving a unique pointer to another unique pointer transfers ownership, invalidating the original. This allows compile-time memory validation with no extra performance impact.
```loom
unique string myString = "Hello, World!";
unique string passed = myString;

println(myString); // Compile Error, myString is not owner!
println(passed); // "Hello, World!"
```

### Shared Pointers
Shared Pointers provide shared ownership of an object. Moving a shared pointer to another shared pointer increments an internal instance counter, allowing both the original and the current to be used.
```loom
shared string myString = "Hello, World!";
shared string passed = myString;

println(myString); // "Hello, World!"
println(passed); // "Hello, World!"
```

## Array Types
Arrays are a way to represent a fixed-length sequence of types. Arrays are Value Types.
```loom
i32[5] arr = { 2, 3, 1, 6, 2 };
println(arr[3]); // 6
```
For a dynamically sized sequence, or a reference type equivalent to an array, `Vector<T>` is used.

## Built-In Types
Loom has various predefined types that are used heavily.
| Type | Description |
|---|---|
| `void` | Represents the absence of a value. |
| `bool` | Boolean value, either `true` or `false`. |
| `char` | Single Unicode scalar value. |
| `string` | Sequence of Unicode characters with UTF-8 encoding. |
| `iptr` | Signed integer type whose size matches the target platform's pointer size. |
| `i8` | Signed 8-bit integer. |
| `i16` | Signed 16-bit integer. |
| `i32` | Signed 32-bit integer. |
| `i64` | Signed 64-bit integer. |
| `u8` | Unsigned 8-bit integer. |
| `u16` | Unsigned 16-bit integer. |
| `u32` | Unsigned 32-bit integer. |
| `u64` | Unsigned 64-bit integer. |
| `f32` | 32-bit floating-point number. |
| `f64` | 64-bit floating-point number. |