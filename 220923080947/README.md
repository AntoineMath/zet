# Final method Java  
A final method implemented in a parent class **cannot be overriden** by its children classes

```java
class  Base {
   int a;
   public  Base(int i) {
     a = i;
   }
   public Base() {
     a = 1000;
   }
   final  public void Show() {
     System.out.println(a);
   }
}
class D extends Base {
    public void Show() {
        System.out.println(super.a);
    }
}
class Abstract  {
   public static void main(String argv[]) {
      new Base(50);
  }
}

```
#javac Abstract.java 
Abstract.java:14: Final methods can't be overriden. Method void Show() is final in class Base.
    public void Show() {
1 error
```

## References
    #java
    
