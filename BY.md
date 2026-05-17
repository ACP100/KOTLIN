#delegate

```kotlin
import kotlin.reflect.KProperty

fun main() {
	var hello : String?  by delegate<String>()
// 	var hello: Int = 5
	hello = "5"
    print("$hello") 
}



class delegate <T>{
    var  storedValue : T? = null
    operator fun getValue(thisRef: Any?, property: KProperty<*>): T?  {
        println("HELLO MU ${storedValue?.javaClass?.simpleName}")
        if( storedValue == null ) print ("lamo null")
        return storedValue 
}
    operator fun setValue(thisRef: Any?, property: KProperty<*>, newValue: T?) {
        println("this is setter")
        storedValue = newValue
    }
}
```


```
this is setter 
HELLO MU String 
5
```