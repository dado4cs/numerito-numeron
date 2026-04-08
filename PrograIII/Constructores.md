# Constructors in C++

## Copy Constructor
A copy constructor is defined when the first parameter of the constructor is a reference to the same class type.

```cpp
class Student {
public:
    Student() = default;           // Default constructor
    Student(const Student& other); // Copy constructor
    // ...
private:
    string name;
    vector<int> grades;
};

// Implementation of the copy constructor
Student::Student(const Student& other) {
    name = other.name;
    grades = other.grades;
}
```

If you do not define a copy constructor, the compiler will provide a **synthetic copy constructor** that performs a member-wise copy.

## Move Constructor (C++11)
The move constructor allows you to "move" resources from one object to another instead of copying them. This is much more efficient when dealing with large objects like matrices or vectors that use dynamic memory.

**Advantages:**
- Avoids unnecessary copies of large amounts of data.
- Provides a significant performance boost for classes using dynamic memory.

### **Lvalues and Rvalues**
To understand move constructors, you must understand value categories:
- **Lvalue:** An object that has a persistent location in memory (it has a name, e.g., `int x = 10;`).
- **Rvalue:** A temporary object that does not have a persistent name (e.g., the literal `3` or the result of `a + b`).

### **Rvalue References (`&&`)**
An rvalue reference is a reference that can only bind to a temporary object. It is declared using two ampersands (`&&`).

```cpp
int i = 42;
int &&r1 = 8;         // OK: 8 is an rvalue
int &&r2 = i * 42;    // OK: the result of i * 42 is an rvalue
const int &r3 = i * 42; // OK: a const lvalue reference can bind to an rvalue
```

**Note:** You cannot bind an rvalue reference directly to an lvalue.
```cpp
int &&i = 7;
int &&j = i;        // Error: i is an lvalue
int &&k = std::move(i); // OK: std::move casts lvalue to rvalue reference
```

## Move Constructor Implementation
The move constructor "steals" the resources from the source object and leaves it in a valid but empty state.

```cpp
class DynamicArray {
    int* data;
    size_t size;
public:
    // Move constructor
    DynamicArray(DynamicArray&& other) noexcept 
        : data(other.data), size(other.size) {
        other.data = nullptr; // Leave source in a safe state
        other.size = 0;
    }
};
```
The `noexcept` keyword is crucial for performance and correctness in STL containers.
