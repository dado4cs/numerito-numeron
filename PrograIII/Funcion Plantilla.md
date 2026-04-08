Este tipo de función nos permite generar distintas versiones de sí misma dependiendo del tipo de dato que necesitemos:

```c++
template<typename T>
bool comparar(T x, T y){
	return x < y;
}
```
El compilador device el tipo de valor de T

```c++
int main(){
	cout << comparar(3.4,7.6) << endl;
	cout << comparar(3,4) << endl;
}
```