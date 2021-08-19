# Código random

```kotlin
val line = readLine()!!
```

```kotlin
val name = readLine()
println("What a great name you have, $name!")
```

```kotlin
val scanner = Scanner(System.`in`)
val name = scanner.nextLine()
```

```kotlin
val num1 = scanner.nextLine().toInt()
```

```kotlin
val age = (remainder3 * 70 + remainder5 * 21 + remainder7 * 15) % 105
```

```kotlin
val max = scanner.nextInt()

for (i in 0..max) {
    println("$i!")
}
```

```kotlin
fun test() {
    println("Let's test your programming knowledge.")
    println("Why do we use methods?")

    val alternativas = arrayListOf("To repeat a statement multiple times.",
        "To decompose a program into several small subroutines.",
        "To determine the execution time of a program.",
        "To interrupt the execution of a program.")

    for (i in 0 until alternativas.size) {
        println("${i+1}. ${alternativas[i]}")
    }

    val eleccion = readLine()?.toInt()

    when (eleccion) {
        2 -> {println("Congratulations, have a nice day!")}
        1, 3, 4 -> {println("Please, try again.")}
    }
}
```

```kotlin
fun main() {
    val x = readLine()!!.toInt()
    
    println(if (x % 2 == 0) {
        "EVEN"
    } else {
        "ODD"
    })
}
```

```kotlin
fun main() {
    val x = readLine()!!.toInt()
    println(if (x % 2 == 0) "EVEN" else "ODD")
}
```

```kotlin
fun main() {
    val nums = arrayOf(1, 2, 3, 4)
    
    nums.map{x: -> x * 5}
        .forEach{x: -> println(x)}
}
```

```kotlin
fun main() {
    val nums = arrayOf(1, 2, 3, 4)

    nums.map{x -> x * 5}
        .forEach(::println)
}
```

```kotlin
fun main() {
    val x = Random()
        .ints(1000, 1, 500)
        .filter{x -> x % 2 == 0}
        .map{x -> x.toDouble().pow(2.0).toInt()}
        .sorted()
        .boxed()
        .collect(Collectors.toSet())

    println(x)
}
```

```kotlin
fun main() {
    // write your code here
    val num = readLine()!!.toInt()
    
    println(if (num < 0) "negative" else if (num > 0) "positive" else "zero")
}
```

```kotlin
fun main() {    
    // write your code here
    val a = readLine()!!.toInt()
    val b = readLine()!!.toInt()
    val h = readLine()!!.toInt()

    println(if (h < a) "Deficiency" else if (h > b) "Excess" else "Normal")
}
```

```kotlin
fun main() {
    // write your code here
    val num1 = readLine()!!.toInt()
    val num2 = readLine()!!.toInt()
    val num3 = readLine()!!.toInt()
    
    println(num1 in num2..num3)
}
```
