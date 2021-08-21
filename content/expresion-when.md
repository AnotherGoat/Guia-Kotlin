

val resultado = when {
    num > 0 -> "Positivo"
    num < 0 -> "Negativo
    else -> "Cero"
}

fun transform(color: String): Int {
    return when (color) {
        "Red" -> 0
        "Green" -> 1
        "Blue" -> 2
        else -> throw IllegalArgumentException("Invalid color param value")
    }
}
