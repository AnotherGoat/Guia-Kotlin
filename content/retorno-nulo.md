# Retorno nulo

Al igual que con las variables, intentar hacer que una función retorne un valor `null` no funcionará.

```kotlin
fun retornarNulo() {
    return null
}
```

En su lugar, indicará un problema debido al tipo de retorno `Unit`.

```text
Kotlin: Null can not be a value of a non-null type Unit
```

En el caso de especificar otro tipo de retorno, se mostrará un mensaje de error similar.

```kotlin
fun retornarNulo(): Float {
    return null
}
```

Aunque claramente, indicará el tipo de retorno distinto.

```text
Kotlin: Null can not be a value of a non-null type Float
```

## Solución

Al igual que como sucede con variables, la solución
