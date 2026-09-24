# Functions
Functions are reusable blocks of code that can optionally accept input and produce output.

## Function Declaration
A Function declaration consists of optional modifier keywords, a specified return type, a unique function name, a parameter list enclosed in parentheses, and a function body defining its behavior.

```loom
i32 Add(i32 a, i32 b) 
{
    return a + b;
}
```

By default, functions defined at the module level are static, whereas functions defined within a type are instance-based. Type-enclosed functions can be explicitly declared static by applying the `static` modifier.

## Parameters
Functions can accept input through **parameters**. Parameters define the values that a function expects to receive when it is called.

```loom
void PrintInput(i32 num)
{
    println(num);
}
```

## Returning
Functions can produce output by returning a value using the **return statement**.

```loom
i32 GetNumber()
{
    return 10;
}
```

A function must specify its return type when it returns a value. Functions that do not return a value must use void.