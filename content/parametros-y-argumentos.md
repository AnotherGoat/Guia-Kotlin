# Parámetros y argumentos

Dos conceptos similares e importantes al momento de trabajar con funciones son parámetros y argumentos.
Un parámetro es usado al momento de definir una función y sirve para especificar las variables que se le pueden entregar a la función y que se usarán en el cuerpo de ésta.
Un argumento es un literal o una expresión que indica el valor que se le da a un parámetro al momento de llamar una función.

## Parámetros

Los parámetros de una función se definen utilizando notación similar a la del lenguaje de programación [Pascal](https://en.wikipedia.org/wiki/Pascal_(programming_language)), que tiene el formato `nombre: tipo`.
Cada parámetro viene separado por comas `,` en la declaración de una función.

```kotlin
fun sumar(num1: Int, num2: Int) {
    println(num1 + num2)
}
```

Los parámetros de una función no necesitan ser del mismo tipo, pero su tipo debe especificarse.

```kotlin
fun mostrar(mensaje: String, resultado: Boolean) {
    println("$mensaje: $resultado")
}
```

## Argumentos

Cuando se llama una función, esta operación se realiza entregándole argumentos.
Por defecto, se espera que los argumentos estén en el mismo orden que el de los parámetros.

```kotlin
fun main() {
    mostrar("Día soleado", true)
}
```

Como a la función `mostrar()` se le entregaron argumentos de forma correcta, se muestra la salida correctamente.

```text
Día soleado: true
```

Los argumentos deben cumplir las restricciones que exigen los parámetros, como algo que ocurre en la función `duplicar()`.

```kotlin
fun duplicar(x: Int) {
    println(2 * x)
}
```

Debido a que se especificó que el parámetro `x` es de tipo `Int`, no se puede llamar a la función utilizando otro tipo, como por ejemplo `String`.

```kotlin
fun main() {
    duplicar("hola")
}
```

El código anterior no se podrá ejecutar y se indicará esto en la consola.

```text
Kotlin: Type mismatch: inferred type is String but Int was expected
```
