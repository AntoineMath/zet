---  
id: 202301310751  
share: true  
---  
# Constructor dependency injection  
Type of injections  in Spring:  
- Setters and Getters  
- Field  
- Constructor  
  
The preferable way of doing dependency injection is on **constructor**. Because to initialize the object, we are sure that the dependencies have to exist, thus avoiding initializing an object without its dependencies.  
It prevents the "NullPointerException" thrown by Spring IoC.  
  
  
  
  
## References  
  
## Litterature note  
  
