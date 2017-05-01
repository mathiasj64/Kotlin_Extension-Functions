# Kotlin_Extension-Functions

Extension functions can as the name indicates extend a class with a function.

In the following example we used extension functions to extends the String class with a new method ConvertSpacesToUnderscores().

Normally we would do something like this without the use of extension functions:

```kotlin

fun convertSpacesToUnderscores(str: String): String {
 return str.replaceAll(" ", "_")
}

println(convertSpacesToUnderscores("Hello_Class!_How_are_you?"))

//prints: Hello_Class!_How_are_you?
```
Now with a class extended with a function instead:

```kotlin

fun String.convertSpacesToUnderscores(): String {
  return this.replaceAll(" ","_")  
}

println("Hello Class! How are you?".convertSpacesToUnderscores())

//prints: Hello_Class!_How_are_you?
```

## Scope

The extension function example given above can also have effect on other classes if you like in Java import the package: package org.defaultname.samples
