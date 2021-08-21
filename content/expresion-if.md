# Expresiones

Kotlin permite que la mayoría de estructuras de control se utilicen como expresiones.
Esto significa que se pueden utilizar dentro de métodos y asignarse a variables.

## Expresión if

Al usar una expresión condicional con la palabra clave `if` donde iría un literal, se puede usar como una función que retorna un resultado específico.

```kotlin
val semaforo = "Verde"

val resultado = if (semaforo == "Verde") {
    "Puedes pasar"
} else if (semaforo == "Amarillo") {
    "Ten cuidado"
} else {
    "Espera a que llegue tu turno"
}
```

Esto también significa que puede usarse una expresión if como argumento de funciones.

```kotlin
val numero = -22

println(if (numero >= 0) "Positivo" else "Negativo")
```

En este caso se usa `if` dentro del método `println()`.
