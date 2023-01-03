---  
id: 202301031521  
share: true  
---  
# Interface vs Abstract class  
- Consider using the interface when our problem makes the statement **"A is capable of \[doing this\]"**  
```java  
public interface Sender {  
    void send(File fileToBeSent);  
}  
  
public class ImageSender implements Sender {  
    @Override  
    public void send(File fileToBeSent) {  
        // image sending implementation code.  
    }  
}  
```  
- Consider using abstract classes and inheritance when our problem makes the evidence **“A is a B”**  
```java  
public abstract class Vehicle {  
      
    protected abstract void start();  
    protected abstract void stop();  
    protected abstract void drive();  
      
    // standard getters and setters  
}  
  
public class Car extends Vehicle {  
  
    @Override  
    protected void start() {  
        // code implementation details on starting a car.  
    }  
  
    @Override  
    protected void stop() {  
        // code implementation details on stopping a car.  
    }  
  
    @Override  
    protected void drive() {  
        // code implementation details on start driving a car.  
    }  
}  
```  
  
  
  
## References  
	https://www.baeldung.com/java-interface-vs-abstract-class  
	#java 