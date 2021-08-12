# Variables mutables

Las variables se utilizan para almacenar datos, con el fin de poder trabajar con ellos, reutilizarlos y modificarlos como se desee.

Cada variable tiene un tipo de dato, que define el tipo de información que contiene.
A continuación se muestran algunos ejemplos de variables, declaradas con la palabra clave var.

```kotlin
var num = 100
var saludo = "Hola"
var x = 'x'
var esPosible = true
```

# Reasignación de valores

Las variables mutables pueden ser utilizadas dentro de funciones y su valor se puede reasignar durante la ejecución del programa.

Al momento de reasignar el valor de una variable no es necesario volver a utilizar la palabra var, ya que esta sólo se utiliza al momento de declararla.

```kotlin
fun main() {
    var num = 1000
    println(num)
    
    num = 9999
    println(num)
}
```

El código mostrado arriba muestra la siguiente salida:

```
1000
9999
```
