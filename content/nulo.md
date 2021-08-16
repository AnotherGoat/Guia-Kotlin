# Seguridad contra nulos

Una de las fortalezas de Kotlin comparado con Java es la seguridad contra valores nulos.

## Valor nulo

La palabra clave `null` hace referencia al valor nulo, es decir, algo que no contiene nada o a lo que no se le ha asignado un valor.
Se puede utilizar para darle valor a variables.

```kotlin
var nulo = null
```

Hasta el momento no se aprecia una diferencia con respecto a otros lenguajes de programación.
Ahora veamos qué ocurre si se le intenta dar un valor nulo a una variable a la que se le indicó el tipo.

```kotlin
var nulo: String = null
```

Esta vez, se mostrará el siguiente error en la consola:

```text
Kotlin: Null can not be a value of a non-null type String
```

Aquí se puede ver en acción el funcionamiento básico de la protección contra valores nulos y el motivo por el cual se recomienda indicar el tipo de dato de las variables.

## Explicación

Lo que sucede en realidad es que Kotlin infiere el tipo de `null` al declarar la variable `nulo` en el primer caso.
Intentar darle un valor no nulo a esta variable no funcionará.

```kotlin
var nulo = null
nulo = 123
```

El resultado se indicará en un mensaje de este tipo.

```text
Kotlin: The integer literal does not conform to the expected type Nothing?
```

Lo mismo ocurre en el caso anterior.

Esto representa una de las medidas básicas que Kotlin toma para evitar valores nulos y anteponerse a excepciones del tipo `NullPointerException`, que a veces pueden ser muy molestas en otros lenguajes.
Sin embargo, esta es solo una de las muchas formas en las que Kotlin permite trabajar y evitar valores nulos.
