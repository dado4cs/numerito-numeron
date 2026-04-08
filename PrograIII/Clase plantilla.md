# Class Templates
A major difference between a class template and a [[Funcion Plantilla|function template]] is that the compiler cannot always deduce the template parameter for a class; you must specify it explicitly during instantiation.

```cpp
int main(){
    MiClase<int> c1;   // Explicitly specifying 'int'
    MiClase<float> c2; // Explicitly specifying 'float'
    MiClase<char> c3;  // Explicitly specifying 'char'
}
```

## Example
When defining a class template, you use the `template <typename T>` prefix.

```cpp
#include <iostream>
using namespace std;

template <typename T>
class Pair {
    T _a, _b;
public:
    Pair(T a, T b) {
        _a = a;
        _b = b;
    }
    T Max();
};

// Definition of a member function outside the class template
template <class T>
T Pair<T>::Max() {
    return (_a > _b) ? _a : _b;
}

int main() {
    Pair<float> obj(1.3f, 6.2f);
    cout << "Max: " << obj.Max() << endl;
    
    return 0;
}
```

## Key Points
- **Instantiation:** The process of creating a specific class from a template (e.g., `Pair<int>`).
- **Template Parameters:** Can be types (`typename T`) or non-type parameters (e.g., `template <typename T, int Size>`).
- **Implementation:** Member functions defined outside the class must also include the template prefix.
