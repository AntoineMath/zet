---  
id: 202301081317  
share: true  
---  
# Static in Java  
  
**Very good summary** : https://www.baeldung.com/java-static#:~:text=In%20the%20Java%20programming%20language,all%20instances%20of%20the%20class  
  
## Static field (Class variable)  
- When we declare a field _static_, exactly a single copy of that field is created and shared among all instances of that class.  
- We don't need object reference to access them : `MyClass.myStaticVariable`.  
- We can acess static fields without object initialization  
- Static variables are stored in the heap memory.  
  
  
## Static method (Class method)  
- No reference needed, shared across all the class objects.  
- _static_ methods can access all _static_ variables and other _static_ methods  
- **_static_ methods can't access instance variables and instance methods directly.** They need some object reference to do so.  
  
  
See also : static inner classes and static blocks.   
  
  
## References  
https://www.baeldung.com/java-static#:~:text=In%20the%20Java%20programming%20language,all%20instances%20of%20the%20class.  
  
