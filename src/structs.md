# Structs
Structs are user-defined types used for grouping related symbols together. They are similar to classes, but are Value Types and cannot use inheritance.

## Struct Declaration
A Struct declaration consists of optional modifier keywords, the `struct` keyword, a unique struct name, and then it's body.

```loom
export struct MyStruct
{
    i32 number = default;
    
    public i32 GetNumber()
    {
        return number;
    }
}
```