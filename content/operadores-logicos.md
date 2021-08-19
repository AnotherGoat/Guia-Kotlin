# Operadores lógicos

Los operadores lógicos se utilizan para crear condiciones complejas agrupando condiciones más simples.
Estos operadores son and, or y not.

## Operador and

El operador and se escribe como `&&` y se evalúa como `true` si ambas condiciones se cumplen.

```kotlin
println(1 == 1 && 2 == 2) // true
println(5 > 3 && 3 > 4) // false
```

## Operador or

El operador or se escribe como `||` y se evalúa como `true` si al menos una de las condiciones se cumple.

```kotlin
println(1 == 1 or 2 == 2) // true
println(5 > 3 or 3 > 4) // true
```

## Operador not

El operador not se escribe como `|` e invierte la condición que le sigue.

```kotlin
print(not 1 > 100) // true
```
