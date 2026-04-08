La gran diferencia con una [[Funcion Plantilla]] es que el compilador no puede deducir el parámetro template:

```c++
int main(){
	MiClase<int> c1;
	MiClase<float> c2;
	MiClase<char> c3;
}
```

Ejemplo:

```c++
template <typename T>
class Pair{
	T _a, _b;
public:
	Pair(T a, T b){
		_a = a;
		_b = b;	
	}
	T Max();
};

template <class T>
T Pair<T>::Max (){
	return (_a > _b) ? _a : _b;
}


int main(){
	Pair<float> obj(1.3, 6.2);
	cout << obj.Max() << endl;
	
	return 0;
}

```