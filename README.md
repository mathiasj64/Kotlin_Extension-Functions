# Kotlin_Extension-Functions

Extension functions can as the name indicates, extend a class with a function.

In the following example we used extension functions to extends the String class with a new method ConvertSpacesToUnderscores().

Normally we would do something like this without the use of extension functions:

```kotlin

fun convertSpacesToUnderscores(str: String): String {
 return str.replaceAll(" ", "_")
}

println(convertSpacesToUnderscores("Hello Class! How are you?"))

// Prints: Hello_Class!_How_are_you?
```
Now with a class extended with a function instead:

```kotlin

fun String.convertSpacesToUnderscores(): String {
 return this.replaceAll(" ","_")  
}

println("Hello Class! How are you?".convertSpacesToUnderscores())

// Prints: Hello_Class!_How_are_you?
```

## Extension properties

Similarly to functions, Kotlin also supports extensions on properties
The example below shows an extension property

```
class Person(val name: String, var age: Int)

val Person.dogAge : Int
  get() = this.age * 7

fun main(args: Array<String>)
{
    val kurt = Person("Kurt", 21)
    println(kurt.dogAge)
}

// Prints 147
```

In the example we've applied 

## Scope

The extension function example given above can also have effect on other classes if you like in Java import the package: package org.defaultname.samples. It is ideal to create a seperate kotlin file with all your extension functions needed. Then you're able to import the file and use your extension functions anywhere.

## Why and when to use it?
