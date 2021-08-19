# Operadores de comparación

Kotlin permite comparar datos mediante operadores de comparación.
Las expresiones que usan comparadores retornan un `Boolean` que indica el resultado de la operación.

## Operadores básicos de comparación

Los operadores básicos de comparación son los siguientes:

- Igual `==`: Se evalúa como `true` si ambos elementos son iguales.
- Distinto `!=`: Se evalúa como `true` si ambos elementos son distintos.
- Mayor que `>`: Se evalúa como `true` si el primer elemento es mayor.
- Menor que `<`: Se evalúa como `true` si el primer elemento es menor.
- Mayor o igual que `>=`: Se evalúa como `true` si el primer elemento es mayor o igual
al segundo.
- Menor o igual que `<=`: Se evalúa como `true` si el primer elemento es menor o igual
al segundo.

En los casos contrarios, los resultados se evalúan como `false`.
El resultado de una comparación se puede mostrar en pantalla directamente.

```kotlin
fun main() {
    println(1 == 1) // true
    println(4 != 4) // false
    println(10 > 10) // false
    println(-1 < 0) // true
    println(3 >= 3) // true
    println(0 <= -10) // false
}
```

También se conocen como operadores relacionales.

## Comparación de cadenas de caracteres

Los operadores `==` y `!=` funcionan entre strings como se esperaría.

```kotlin
fun main() {
    println("agua" == "aceite") // false
    println("huevo" == "huevo") // true
}
```

Pero los operadores `>`, `<`, `>=` y `<=` cambian su funcionamiento.
Estos comparan cadenas lexicográficamente (por orden alfabético), donde las palabras que están después se consideran "mayores".

```kotlin
println("a" < "d") // true
println("b" > "c") // false
println("Ana" > "Alicia") // true
```

Las letras mayúsculas siempre irán antes (son "menores") que las minúsculas al ordenarlas alfabéticamente.

```kotlin
println("A" == "a") // false
println("B" < "b") // true
println("a" > "Z") // true
```

En específico, Kotlin compara los valores [Unicode](https://unicode-table.com/en/) para ordenar las cadenas de texto.
