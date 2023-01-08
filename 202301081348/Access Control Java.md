---  
id: 202301081348  
share: true  
---  
# Access Control Java  
  
## Controlling Access of a Class  
  
| Modifier    | Class | Package | Subclass | Entire program |  
| ----------- | ----- | ------- | -------- | -------------- |  
| public      | Y     | Y       | Y        | Y              |  
| no modifier |   Y    |     Y    |      N    |         N       |  
  
## Controlling Access to Members of a Class  
  
| Modifier    | Class | Package | Subclass | Entire program |  
| ----------- | ----- | ------- | -------- | -------------- |  
| public      | Y     | Y       | Y        | Y              |  
| protected   |  Y     |   Y      |    Y      |        N        |  
| no modifier |   Y    |     Y    |      N    |         N       |  
| private         Y   |    N   |    N     |     N     |      N          |  
  
  
## Reminder on packages  
project **/**  
	**a/**  
		ClassA1.java **(no modifier)**  
		ClassA2.java (public)  
		**b**/  
		    ClassB.java (public)  
    **c/**  
		ClassC.java (public)  
  
a,  a.b, and c are different packages.    
ClassB, ClassC and ClassA2 are accessible from everywhere (public).  
ClassA1 is accessible only in package a, **not in a.b**. So only ClassA2 can acess ClassA1.    
  
## References  
https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html  
	#java  
  
