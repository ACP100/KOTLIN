``` kotlin
fun main() {    
	val x = 4    
	when (x) {        
	2, 3, 5, 7 -> println("x is a prime number between 1 and 10.")        
	in 1..10 -> println("x is a number between 1 and 10, but not a prime number") 
	is Int -> println("hello") 
	else -> println("x isn't a prime number between 1 and 10.")    }}
```


in 1...10 but not 2,3,5,7 



```kotlin
val trafficcolour = "black"
val x = 
 if (trafficcolour = "red") "sstop"
 else if (trafficcolour =  "yellow") "almost sotop"
 else "hello"
```


```kotlin
val trafficcolour = "black"

val x = 
	when (traficcolour){
		"red" -> "pain"
	}
	
print("$x")
```





# fxn type parameter

In Kotlin, **`onImageClick: () -> Unit`** is a function type parameter that turns the `LemonTextAndImage` Composable into a reusable template by letting the caller decide exactly what happens when the user interacts with the UI. Inside the Composable, this parameter is passed directly to the standard button component using **`onClick = onImageClick`**, meaning the button is wired to execute whatever "recipe" of code was handed to it. This is why, in your `LemonadeApp`'s `when` block, you can pass different logic for each step—such as **`onImageClick = { currentStep = 2 }`** to move forward or **`onImageClick = { currentStep = 1 }`** to restart—allowing the same UI code to perform completely different actions depending on the state of the app.

