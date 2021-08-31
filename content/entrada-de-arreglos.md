val numbers = IntArray(5) { readLine()!!.toInt() } // on each line single numbers from 1 to 5
println(numbers.joinToString()) // 1, 2, 3, 4, 5




// here we have an input string "1 2 3 4 5"

val numbers = readLine()!!.split(" ").map { it.toInt() }.toTypedArray()
println(numbers.joinToString()) // 1, 2, 3, 4, 5
