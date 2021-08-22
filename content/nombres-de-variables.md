# Nombres de variables

Kotlin aplica ciertas restricciones con respecto a los caracteres que se pueden usar en los nombres de variables.

## Caracteres permitidos

Los únicos caracteres permitidos por defecto son letras, números y guiones bajos `_`.
Además, no se puede comenzar con números.

La excepción a esta regla es si se rodea el nombre con acentos graves `` ` ``, ya que esto permite escapar los caracteres.

Y aún así, esta excepción tiene casos particulares de caracteres que no podrán ser escapados dependiendo del sistema operativo.
Por ejemplo, la máquina virtual de Java (JVM) no permitirá que se escapen los siguientes caracteres: `.`, `(`, `)`, `[`, `]`, `{` y `}`.

Koltin es sensible a mayúsculas y minúsculas, lo que significa que las variables `num`, `Num`, `NUM`, etc. son distintas.

```kotlin
val num = 3
val Num = 5
val NUM = 10

println(NUM)
println(num)
println(Num)
```

## Nombres largos

Los nombres de variables que se componen de más de una palabra pueden ser difíciles de leer.
Existen muchas técnicas para escribirlos de forma más legible.

- Pascal Case: Todas las palabras empiezan con mayúscula.

```kotlin
val VariableDeNombreLargo: String
```

- Camel Case: Todas las palabras empiezan con mayúscula, excepto la primera.
  
```kotlin
val variableDeNombreLargo: String
```

- Kebab Case: Todas las palabras se escriben en minúscula y van separadas por guiones `-`.

```kotlin
val variable-de-nombre-largo: String
```

- Snake case: Todas las palabras se escriben en minúscula y van separadas por guiones bajos `_`.
  
```kotlin
val variable_de_nombre_largo: String
```

- Screaming Snake Case: Todas las palabras se escriben en mayúscula y van separadas por guiones bajos `_`.

```kotlin
val VARIABLE_DE_NOMBRE_LARGO: String
```

Las convenciones del lenguaje prefieren el uso de algunos estilos sobre otros.
En Kotlin, generalmente se usan los estilos Camel Case, Pascal Case y Screaming Snake Case.

## Nombres con espacios

Kotlin permite el uso de espacios en nombres de variables.
Esto es posible al rodear el nombre de la variable con acentos graves `` ` ``.

```kotlin
val `variable de nombre largo`: String
```

Al momento de usar esta variable se deberá rodear el nombre de la misma forma.
