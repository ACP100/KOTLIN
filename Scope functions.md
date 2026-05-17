
# LET
#let
# examle1
```kotlin
fun main() {
    var hello = "heLlo1"
    var hi = hello.let{
        it.reversed()
        it.lowercase()
        println("$it")
    }
    
    print("$hi")
}
```


reversed and lowercase doesn't actually change the value of it i.e. hi.
as only last expression is returned to the original object.
in this case the last expression is:
```kotlin
println("$it")
```

hence the value of hi is what ever println("$it") returns which is kotlin.Unit meaning void i.e. it doesnt really outputs anyything.


# example2
Another example of where let can be used:
```kotlin
fun main () {
	var x : Int? = 2
	var y = x?.let{
		// it = it * 5 // this is wrong 
		it * 5
	}?: 4
	
	print("$y")
}
```

***NOTE** : it inside let is a val and not var that is the reason why the commented part gives out an error.*

So, basically what this does is the following:
```kotlin
fun main () {
	var x : Int? = 2
	var y = mul(x)
	print ("$y")
}

fun mul (x : Int?) : Int  {
	if (x != null) { return x * 5}
	else {return null}
}
```
see how slick it make it look 

observe how well #null  variable is managed by let 


# example3 

now lets take a look at an example which is more realistic -> whcih we might actually use :

let us assume that we are to make a class and ... just look at the code:
```kotlin 
class Student (
	var Name : String,
	var Roll : Int
) 

fun main () {
	var student1 = Student("Ram" , 45)
	student1.let {
		println("${it.Name}")
		println("${it.Roll}") 
	}
}
```


it shows how **Let** can be used for classes and stuffs but it isn't rally efficient in this case.

Hence, we can conclude that **Let** is promarily useful for data manipulation and handling null objects like in example1 and example2

But for the use case of scenarios like in example3, a better approach would be to use : ***apply***