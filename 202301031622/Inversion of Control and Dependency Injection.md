---  
id: 202301031622  
share: true  
---  
# Inversion of Control with Dependency Injection  
  
  
**A bean no longer controls the creation or location of its dependencies.**    
Dependency injection is a process whereby objects define their dependencies  **only through constructor arguments, arguments to a factory method, or properties** that are set on the object instance after it is constructed or returned from a factory method.    
**The container then injects** those dependencies when it creates the bean.   
  
It is the opposite of what is done usually, hence the name Inversion of Control (IoC).  
  
## Dependency Injection (DI)  
- [Constructor-based dependency injection](https://docs.spring.io/spring-framework/docs/3.2.x/spring-framework-reference/html/beans.html#beans-constructor-injection "Constructor-based dependency injection")   
```java  
public class SimpleMovieLister {  
  
  // the SimpleMovieLister has a dependency on a MovieFinder_  
  private MovieFinder movieFinder;  
  
  // a constructor so that the Spring container can 'inject' a MovieFinder_  
  public SimpleMovieLister(MovieFinder movieFinder) {  
      this.movieFinder = movieFinder;  
  }  
  
  // business logic that actually 'uses' the injected MovieFinder is omitted..._  
}  
```  
-  [Setter-based dependency injection](https://docs.spring.io/spring-framework/docs/3.2.x/spring-framework-reference/html/beans.html#beans-setter-injection "Setter-based dependency injection")  
```java  
public class SimpleMovieLister {  
  
  // the SimpleMovieLister has a dependency on the MovieFinder_  
  private MovieFinder movieFinder;  
  
  // a setter method so that the Spring container can 'inject' a MovieFinder_  
  public void setMovieFinder(MovieFinder movieFinder) {  
      this.movieFinder = movieFinder;  
  }  
  
  // business logic that actually 'uses' the injected MovieFinder is omitted..._  
}  
```  
  
## Dependency resolution process  
The IoC container performs bean dependency resolution as follows:  
  
1.  The `ApplicationContext` is created and initialized with configuration metadata that describes all the beans. Configuration metadata can be specified via XML, Java code or annotations.  
      
2.  For each bean, its dependencies are expressed in the form of properties, constructor arguments, or arguments to the static-factory method if you are using that instead of a normal constructor. These dependencies are provided to the bean, _when the bean is actually created_.  
      
3.  Each property or constructor argument is an actual definition of the value to set, or a reference to another bean in the container.  
      
4.  Each property or constructor argument which is a value is converted from its specified format to the actual type of that property or constructor argument. By default Spring can convert a value supplied in string format to all built-in types, such as `int`, `long`, `String`, `boolean`, etc.  
  
## @Autowired  
We can use @Autowired thanks to the [[@SpringBootApplication]] annotation. No need to use getters and setters anymore.  
  
> **it will automatically scan the components in the current package and its sub-packages**. Thus it will register them in Spring's Application Context, and allow us to inject beans using _@Autowired_.  
> https://www.baeldung.com/spring-autowire  
  
## References  
	https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-factory-collaborators  
	https://www.baeldung.com/spring-autowire  
	#java #spring #dependency-injection #ioc  
  
  
  
  
## References  
  
## Litterature note  
  
