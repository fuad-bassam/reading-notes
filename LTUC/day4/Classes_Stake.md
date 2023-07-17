

# classes
----
![image](../image/day4/day4_classes-and-objects_2.png)
 


classes are the template (blueprint) for creating element each element have the same properties with different value called `Object`.

and the classes can take attributes from other classes and that is what we called `inheritance`.

this `Object` is an instance of Class have its own data but in his Class format, we can create object form class in `Reference way`.
 
this `Reference Type` is the way that we told the compiler that this Object has the template for the specific class.

`ClassName object = new ClassName();`


so if we want to create an object we need to give every object data mostly not like the other object and in class, there is a method that does this assign this data called `Constructor` and this constructors method must have the same name as the class and have the attributes that it will assign it.
Example

```
public class Class1
{
    string attribute1;
    string attribute2;

   public Class1(string attribute11, string attribute22)
   {
      attribute1 = attribute11;
      attribute2 = attribute21;
   }
```
and also for constructor, there is another type it will work fast and get called first and most used for static property for make default data called `Static Constructor`, but this Constructor shouldn't have parameters, we call each parameter with a separate `setter` and `getter`.
this  `setter` and `getter` way it is more secure and the data can reach in the better way we call it `Properties`.

Example
```
public double FirstName
   {
       get { return _firstName ; }
       set {
          _firstName = value ;}
   }
```
 **Hint:-**

  -  we start `firstName` with `_` and we use `camel case` that way programer used to say that is a private cant accesses from out of class.
  - we use FirstName to reach the privet properties  _firstName and the programmer uses `pascal case` to write it.
  - `value` is the way that `set` have the data ` ClassName.FirstName = "fuad";` the `value` have **fuad** to but in setter.


**Auto-implemented properties.**
```
   public string Name{ get; set; }

```

## Stack vs Heap
----  

`stack`: we use it to store local variables, and we push and pop data in stack Last data in First data Out `LIFO`and when the scope is done the stake will release.
`Heap`: we use it for storing reference variables, Class instances (object) and strings.
and when the contain is null `Garbage Collection` **(GC)** will empty the Heap. 

![image](../image/day4/day4_StackAndHeap.jpg)
------