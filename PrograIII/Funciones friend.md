# Friend Declarations and Templates
When a class template contains a `friend` declaration, the relationship between the class and the friend (function or class) depends on whether the friend itself is a template.

## Friend Non-Template
A regular class or function can be a friend to all instances of a class template.

```cpp
template <typename T>
class Box {
    friend void printInfo(); // printInfo is a friend to Box<int>, Box<float>, etc.
    T data;
};
```

## Template Friend
A class template or function template can be a friend to another class template. This relationship can be specialized:
- **One-to-one:** A specific instance of a template is a friend to a specific instance of another template.
- **One-to-many:** All instances of a template are friends to a specific instance of another template.

### Example: One-to-one
```cpp
template <typename T> class Foo; // Forward declaration

template <typename T>
class Bar {
    friend class Foo<T>; // Only Foo<int> is a friend of Bar<int>
};
```

### Example: One-to-many
```cpp
template <typename T>
class Bar {
    template <typename X> friend class Foo; // All instances of Foo are friends of Bar<T>
};
```
The `friend` declaration allows the friend function or class to access **private** and **protected** members of the host class.
