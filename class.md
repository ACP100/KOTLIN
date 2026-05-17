```kotlin
open class SmartDevices (name: String ,  category : String){
	open fun makeSmartDecision (dcsn : Int){
        println("i am making $dcsn smart decisions")
    }
	open var DeviceType = "hello"
}


class SmartRemote (DeviceName : String , DeviceCategory : String) : SmartDevices (name = DeviceName , category = DeviceCategory){
    fun ChannelChange (noOfChannels : Int ){
        println("i am increasing $noOfChannels number of channels")
    }
    override var DeviceType = "smart remote"
    
    override fun makeSmartDecision(dcsn : Int){
        super.makeSmartDecision(dcsn)
		println("hello from remote")
    }
}  

fun main () {
	val heigt = SmartDevices ("hello" , "hi") 
    val remote = SmartRemote("tv remote" , "remote control")
    remote.makeSmartDecision(2)
    remote.ChannelChange(2)
    remote.ChannelChange(1)
 	println("${remote.DeviceType}")   
}

```

o/p
```
i am making 2 smart decisions hello from remotei am increasing 2 number of channels i am increasing 1 number of channels smart remote
```