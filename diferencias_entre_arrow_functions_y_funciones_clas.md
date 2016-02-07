# Diferencias entre arrow functions y funciones clásicas

Una de las novedades más interesantes de ECMAScript 6 son las denominadas **funciones flecha**, o *arrow functions*. Las funciones flecha son, como su nombre indica, definidas mediante una nueva sintaxis que utiliza una "flecha" (`=>`) a la que estarás acostumbrado si has trabajado en otros lenguajes con [*expresiones lamda*](https://msdn.microsoft.com/es-es/library/bb397687.aspx).

Las funciones flecha se comportan de forma sensiblemente distinta a las funciones tradicionales de JavaScript en una serie de detalles que cabe tener presentes:

* **No pueden llamarse con `new`**: Al no tener un método constructor, no pueden ser utilizadas como constructores. Las funciones flecha lanzarán un error cuando se utilicen con `new`.
* **No hay prototipo**: Al no disponer de constructor, tampoco es necesario un prototipo. Por lo tanto, no existirá la propiedad `prototype`en una función flecha.
* **No crean un nuevo contexto**. El valor de `this`, `super`, `arguments` y `new.target` dentro de la función será el mismo que el de la función tradicional (*non-arrow*) más cercana.
* **No puedes cambiar `this`**: El valor de `this` dentro de la función flecha permanece inmutable a lo largo de todo el ciclo de vida de la función.
* **No hay objeto `arguments`**: Tan solo es posible proporcionarle parámetros a una función flecha mediante parámetros nombrados y *rest parameters*.
* **No es posible duplicar parámetros con el mismo nombre**: Tanto en modo estricto como no estricto, a diferencia de las funciones clásicas, que no lo permiten tan solo en modo estricto.