

before using any variable it must be chosen if it is a var or val 

```kotlin
fun add (a : Int , b : Int): Int {
    return a + b
}

fun main() {
    x = add(1,2)
    
}

```
this is wrong as x hasn't been declared as var or val

```kotlin
fun add (a : Int , b : Int): Int {
    return a + b
}

fun main() {
    val x = add(1,2)
    // or var x = add(1,2)
}
```


# when passing default values in functions, you cannot put default value for one and not put for the other 
```kotlin 
fun displayAlertMessage(OS : String = "UNkknownOS", email : String = "invalid email") : String { } //right

fun displayAlertMessage(OS : String = "UNkknownOS", email : String ) : String {} //wrong
```





# sp vs dp


sp and dp is different

`sp` (scalable pixels) is for **text**. For borders, padding, and shapes, you should use `dp` (density-independent pixels). If a user increases their system font size, your text will grow, but your border thickness should stay consistent.





# NULL

#null 
to make sure that the variable is nullable, we need to do the following:
```kotlin
var acp : String? = "hello
// now acp can be a null
```


nullable means that it is able to store no value, a very good example:

you are required to name your favorite actor, if you have one, you just name it but if you do not have one, whatt will  you do?

just write "None"? 

```kotlin
var favorite : String = "None"
// this implies that your favouite actor is named: "none" and not actually none  
```

this is what you should do:

```kotlin
var favorite : String? = null
```


## null facts
- `null` variable doesn't contain any property or method.
-  to ensure that we can use property or method of non-null values of null variables we use :       " **?.** " example :
```kotlin
favourite?.length
```
### Compare Kotlin's safe vs forced access:

| Operator | Name               | Behavior                         | Result when null       |
| -------- | ------------------ | -------------------------------- | ---------------------- |
| `?.`     | Safe call          | Returns null if property is null | `null`                 |
| `!!.`    | Not-null assertion | Forces access, crashes if null   | `NullPointerException` |
| `.`      | Regular access     | Only works on non-null types     | Compile error          |

``` kotlin
if (favoriteActor != null)
```

![[images/Pasted image 20260506105009.png]]

![[images/Pasted image 20260506105104.png]]

![[images/Pasted image 20260506105134.png]]

![[images/Pasted image 20260506105150.png]]


![[images/Pasted image 20260506105207.png]]

![[images/Pasted image 20260506105223.png]]


# ELVIS fxn

provides default values if the variabe is null
```kotlin
var favoriteActor: String? = null
val length
if (favoriteActor != null) {
    length = favoriteActor.length
} else {
    length = 0
}

```

```kotlin
val favoriteActor: String? = null
val length = favoriteActor?.length ?: 0
```





```kotlin
fun whatisyourname (name : String ) 
```


![[Pasted image 20260506110212.png]]
![[Pasted image 20260506110230.png]]

![[Pasted image 20260506110255.png]]

![[Pasted image 20260506110551.png]]
