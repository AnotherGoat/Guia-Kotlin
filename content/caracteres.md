# Caracteres

Un carácter es cualquier símbolo que forma parte de una palabra que se muestra en un computador.

## El tipo Char

Un carácter puede representar un símbolo, una letra o dígito.
Para escribir un carácter se debe escribir un único símbolo entre comillas simples

```kotlin
var letra = 'K'
```

No se deben confundir caracteres con números, como por ejemplo `'5'` y `5`.

```kotlin
val caracter = '5' // Char
val numero = 5 // Integer
```

También se debe dejar claro que los caracteres representan un único símbolo y no múltiples símbolos.
El código mostrado a continuación no es válido.

```kotlin
var texto = 'abc'
```

Para casos como el anterior existe el tipo de dato `String`.

## Ejemplos de caracteres

Ejemplos de caracteres incluyen los siguientes:

- Letras mayúsculas y minúsculas de `'A'` a `'Z'` y de `'a'` a `'z'`.
- Dígitos, de ``0'` a `'9'`.
- Espacios en blanco como por ejemplo `' '`.
- Símbolos como `'$'`, `'%'`, `'&'`, `'#'`, etc.
- Letras de otros alfabetos como `'阿'`, `'λ'` y `'Я'`.

No incluye:

- Emojis como `'😂'`, `'💩'` y `'👻'`.
