


# no dependewncy injection
```kotlin
class FileLogger {
    fun log(msg: String) = println("Saving '$msg' to a physical file...")
}

class UserService {
    // TIGHT COUPLING: UserService creates its own dependency
    private val logger = FileLogger()

    fun registerUser(name: String) {
        // Business logic
        logger.log("User $name registered")
    }
}

fun main() {
    val service = UserService()
    service.registerUser("Aashrutya")
}
```

```
*output*
Saving 'User Aashrutya registered' to a physical file ...

```


aba in this, if i have to use a different logger, then i will have to edit the UserService class itself which does not seem like a big deal now but might be very hard in a production level apps

hmm

then what do i do?

i do this:
# manual deoendency injection

```kotlin

interface Logger {
	fun log (msg: String)
}

class SileLogger : Logger {
	override fun log (msg : String )  = println("this is a sileLogger, hello this is a $msg")
}

class FileLogger : Logger  {
	override fun log (msg : String )  = println("this is a fileLogger, hello this is a $msg")
}

class UserService ( var logger : Logger) // we are aputting a object logger of type Logger 
{ 
	fun registerUser(name : String){
		logger.log("hello this is msg, $name")
	}

}


fun main () {
	val service = UserService(FileLogger())
	service.registerUser("ACP")
} 
```



here i can use whaever logger i want to use without touching the code in UserService

in the hardcoded code, when i needed to change the code i would have had to change the actual hardcoded value in the UserService. 

this is particularly more imortant when we are testing things? we can just swap out the type of logger when calling the UserService




