# Esquema
Se denomina una relación con sus atributos

```
Cervezas(nombre, tipo, grados, ciudad-origen)
Vinos(nombre, tipo, grados, ciudad-origen)
```
La repetición de nombres de atributos entre varias entidades no es un problema, pero se debe desambiguar cada atributo usando el nombre de la relación.

# Dominio 
Asumimos que cada **atributo** tiene un **dominio**. El dominio de forma intuitiva es el tipo de dato.
```
Cervezas(nombre:string, tipo:string, grados:double, ciudad-origen:string)
Vinos(nombre:string, tipo:string, grados:double, ciudad-origen:string)
```

# Instancia
Una instancia de un esquema es un conjunto de tuplas para cada relación de ese esquema. De forma intuitiva es una *fotografía* de la base de datos en algun momento.
Consecuencias de la definición de instancia.
- No hay orden en las filas
- No se puede tener filas duplicadas
# Restricciones
## De integridad
Son restricciones formales, que imponemos a un esquema que todas sus instancias deben satisfacer.
## Llaves
Las llaves son restricciones también. 
### Superllave
Un conjunto de atributos de una relación, forma una **súper llave** si no permitimos que existan dos (o más) tuplas para esa relación con los mismos valores.
### Llave candidata
Un conjunto de atributos de una relación forma una **llave candidata** si es una súper llave y no hay un subconjunto propio de esos atributos que es una súper llave.
### Llave primaria
Se escoge una de las llaves candidatas como **llave primaria**.
### Llave foránea
Es una llave que viene de una llave primaria de otra tabla.

