# Kotlin_Extension-Functions

Extension functions can as the name indicates extends a class with a function.
In the following example we used extension functions to extends the String class with a new method ConvertSpacesToUnderscores().
As the example shows we can now use the new function on any given String.

```kotlin

fun String.convertSpacesToUnderscores(): String {
  return this.replaceAll(" ","_")  
}

println("Hello Class! How are you?".convertSpacesToUnderscores())

//prints: Hello_Class!_How_are_you?
```
