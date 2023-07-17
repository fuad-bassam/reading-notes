# Learning Journal

So today we take about a **dependency injection** and the dependency injection is a way of coding that for **NOT** making our classes depend on another class and to separate code.

We usually use this injection in `controllers` & `Serveses` in this way we dont asign `class -> class` we use it in this way  `class -> interface -> class(serves)`.  

And we can find steps to make everything clear [here](https://github.com/LTUC/amman-401d1-dotnet/blob/main/class-13/resources/di-repository-workshop.md).


Then we take about **SOLID Principles** 

1. Single Responsibility: take about make every class do one thing (class for drive, class for register .....), in this way we easy edit class and reduce bugs 

2. Open-Closed : if we want to edit what the code doing don't delete the previous code instead of that add the new feature on this class, in this way if the code work on the previous code it will still work.

3. Liskov Substitution: if we replace the class in part of code with his child it works, because it has his prosperity and method.

4. Interface Segregation : creating small Interfaces is more powerful than make one big Interface.

5. Dependency Inversion: it is our today subject and the main idea from it to class does NOT depend on another class it depends on the class functionality