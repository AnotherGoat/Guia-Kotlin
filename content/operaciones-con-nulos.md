val files = File("Test").listFiles()

println(files?.size) // size is printed if files is not null

##

val files = File("Test").listFiles()

println(files?.size ?: "empty") // if files is null, this prints "empty"

##

values = ...
val email = values["email"] ?: throw IllegalStateException("Email is missing!")

##

val emails = ... // might be empty
val mainEmail = emails.firstOrNull() ?: ""

##

val value = ...

value?.let {
    ... // execute this block if not null
}

##

val value = ...

val mapped = value?.let { transformValue(it) } ?: defaultValue
// defaultValue is returned if the value or the transform result is null.