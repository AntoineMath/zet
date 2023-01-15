---  
id: 202301151754  
share: true  
---  
# Singleton in Java  
```java  
final public class Singleton {    
    private static Singleton INSTANCE;    
    private Singleton (){};    
    
    static public Singleton getInstance() {    
        if (INSTANCE == null) {    
            return new Singleton();    
        }    
        return INSTANCE;    
    }    
}  
```  
- `final` : the class cannot be subclassed  
- `private` constructor : cannot be called with `new()`  
  
  
	#java #design-patterns