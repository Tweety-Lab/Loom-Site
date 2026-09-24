# Modules
Modules are top-level containers for declarations. A single source file may contain any number of modules.

Modules are used primarily for code organization. Functionally, modules act as Loom's analog to namespaces; however, modules are much more explicit.

## Module Declaration
A Module declaration consists of the `module` keyword followed by the module's identifier and then it's body.
```loom
module MyModule
{
    // Module Contents
}
```

## Module Visiblity
By default, the contents of a module are only accessible within that module. The `export` modifier can be used to make a declaration accessible from other modules.
```loom
export i32 GetNumber() 
{
    return 1 + 1;
}
```

Exported declarations can then be accessed from another module by importing the module with an `import` statement.
```loom
import MyModule;
```
