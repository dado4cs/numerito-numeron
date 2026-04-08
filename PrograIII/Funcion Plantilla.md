# Function Templates
Function templates allow you to define a general version of a function that can work with different data types. The compiler generates specialized versions of the function as needed based on the types used in the calls.

## Example
A simple function to compare two values:

```cpp
#include <iostream>
using namespace std;

template <typename T>
bool is_smaller(T x, T y) {
    return x < y;
}

int main() {
    // The compiler deduces the type of T
    cout << is_smaller(3.4, 7.6) << endl; // T is deduced as double
    cout << is_smaller(3, 4) << endl;     // T is deduced as int
    
    // Explicitly specify the template argument
    cout << is_smaller<int>(5.5, 6.6) << endl; // Compares 5 and 6
    
    return 0;
}
```

## Key Concept: Type Deduction
When you call a function template, the compiler examines the arguments you provide to determine what the template type `T` should be. This is called **template argument deduction**.

- **Note:** For deduction to work, all arguments mapped to the same type `T` must have the exact same type. If you pass an `int` and a `float`, you must either cast one or specify the template argument explicitly (e.g., `is_smaller<double>(3, 4.5)`).
