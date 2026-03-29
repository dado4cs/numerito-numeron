## Constructor de copia
Se define cuando el primer parámetro del constructor es una referencia al tipo de clase.

```c++
class Alumno{
public:
    Alumno() = default;
    Alumno(const Alumno&);
    ...
};

Alumno::Alumno(const Alumno& item){
    nombre = item.nombre; 
    notas = item.notas;
}
```

Si no creamos un constructor de copia el compilador creará un constructor de copia sintético.
## Constructor de movimiento
Permite mover objetos en lugar de copiarlos, tiene las siguientes ventajas:
- Evitar copia innecesaria de grandes cantidades de datos: matrices, estructuras de datos, etc.
- No exiten beneficio alguno si la clase no hace uso de **memoria dinámica**
- Añade más código a la clase

`x = 3`
### **Lvalue** 
Es un objeto que tiene una ubicación en memoria y es identificable. (Ejemplo:  `x` )
### **Rvalue** 
Es un objeto no identificable en memoria. Podemos detectar un Rvalue rápidamente cuando el objeto **no tiene nombre**. (Ejemplo: `3`)

Una referencia de Rvalue es aquella que se vincula únicamente a un Rvalue, es decir a objetos **temporales** en memoria. Se obtiene utilizando `&&` en lugar de `&`.
Ejemplo:

```c++
int i = 42;
int &&c1 = 8;
int &&d1 = i * 42;
const int &d2 = i * 42;
```

Es imposible vincular de manera directa una referencia Rvalue a una variable definida como referencia Rvalue:

```c++
int &&i = 7;
int &&j = i; // esto no funciona
int &&j = move(i); // esto sí
```

La función `move` permite castear un Lvalue a su referencia Rvalue