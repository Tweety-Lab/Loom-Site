# Classes
Classes are user-defined types used for grouping related symbols together. They are similar to structs, but are Reference Types and can use inheritance.

## Class Declaration
A Class declaration consists of optional modifier keywords, the `class` keyword, a unique class name, and then it's body.

```loom
export class MyClass
{
    i32 number = default;
    
    public i32 GetNumber()
    {
        return number;
    }
}
```