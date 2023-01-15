---  
id: 202301151828  
share: true  
---  
# Builder Pattern (in Java)  
```java  
public class FooWithBuilder {    
    private int a;    
    private int b;    
    private String c;    
        
    private FooWithBuilder(int a, int b, String c) {    
    }    
        
    public static class Builder {    
        private int a;    
        private int b;    
        private String c;    
    
        public Builder setA(int a) {    
            this.a = a;    
            return this;    
        }    
        public Builder setB(int b) {    
            this.b = b;    
            return this;    
        }    
        public Builder setC(String c) {    
            this.c = c;    
            return this;    
        }    
    
        public FooWithBuilder build() {    
            return new FooWithBuilder(a, b, c);    
        }    
    }    
}  
  
// in Main.java  
FooWithBuilder.Builder builder = new FooWithBuilder.Builder();  
FooWithBuilder fooWithBuilder = builder  
									.setA(1)  
									.setB(2)  
									.setC("BUILT !")  
									.build();  
```  
