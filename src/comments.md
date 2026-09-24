# Comments
Comments allow developers to add explanatory text to source code that the compiler ignores.

## Simple Comments
Simple comments begin with two forward slashes (`//`). Everything following the `//` on the same line is treated as a comment.
```loom
// My awesome comment!
```

Simple comments are entirely ignored by the compiler and serve only to provide information for developers reading the source code.

## Documentation Comments
Documentation comments are comments that are integrated into development tools and used to provide documentation for symbols such as functions, classes, structs, etc.

Loom uses Doxygen-style documentation comments. Documentation comments begin with three forward slashes (`///`).
```loom
/// @brief The entry point of the program.
i32 main() {}
```

Documentation comments can be displayed by supported tooling, such as when hovering over a symbol in an IDE.