

print : no line gap
println: yes line gap



kotlin = 2
println("$kotlin")



# val and var 
val cannot be cahnged and var can be changed 

```kotlin
val name:String = "Ram"
var address:String = "swarga"

name = "mula"//yes error
addres = "narga" //no error

```

# fxn
```kotlin
fun sum (a : Int, b: Int) : Int {
	return a + b
}


fun sum (a : DataType) : ReturnType {}

ReturnType can be omitted if it doesnt have anyhting it returns

```

if we do:
```kotlin
fun sum (a : Int, b: Int){
	return a + b
}
```
Return type mismatch: expected 'Unit', actual 'Int'. as the function returns Int but when defined , it is defined as Unit, no return type = Unit 



# .background

- color
- shape
- brush


# composable function

this is used for UI


```kotlin
@Composable  
fun GreetingText(message: String, from: String, modifier: Modifier = Modifier) {  
    Column(modifier = modifier) {  
        Spacer(modifier = Modifier.size(36.dp))  
        Text( )  
    }  
}
```

differnt types:

foundation : text image column box 
material: khatra wala
runtime: remember, mutableStateOf : to trigger recompositions based on **state changes**




# ::
In Kotlin, `::` is the **member reference operator** (or class reference).  
It’s used to refer to a function, property, or constructor without invoking it immediately.

**Examples:**
- `::println` → reference to the `println` function
- `MyClass::someMethod` → reference to a method of a specific class
- `::MyClass` → reference to the constructor of `MyClass`

Often used with higher-order functions (e.g., passing `::isBlank` to `filter`).


#annotations
```kotlin
fun secureCall(obj: Any, methodName: String) {
    val method = obj::class.java.getMethod(methodName)
    if (method.isAnnotationPresent(Dangerous::class.java)) {
        println("Confirm dangerous operation?")
    } else {
        method.invoke(obj)
    }
}
```