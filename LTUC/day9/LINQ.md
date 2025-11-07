# LINQ 

it is a that technologies give c# ability to deal with query syntac.
**LINQ spport**
 - objects
 - entities
 - XML
 - dataset

## LINQ write
we can write LINQ in 
- method base

```
Exampe :
 dataType numQuery2 = numbers
                        .Where(`...condition...`)
                            .OrderBy(`...condition...`)
                            .select(`...condition...`);
```

the condetion in this way need to be writen with `lamtha` exepriten (**b => b.FirstName**).
- query base
```
Exampe :
dataType scoreQuery =
               from n in numbers
                 where ...condition...
                 select ...condition...;
```

![img](./Linq.PNG)

---
Most command we use  

1. WHERE 
Used for filtering the requer data from all the data.

```
Exampe:
var cheapBooks = books. Where (b => b. Price < 100); 
```

2. ORDERBY 

Used for ordering the data based on some comditions.

```
Exampe:
var booksCostWise = books.OrderBy (b => b. Price)
```

3. SELECT
Used for selecting property out of an objects or other data.

```
Exampe:
var authors = books. Select (b => b.Author);
```

## Delegate

we use the delegate for passing functions as parameters, and we usually use it to make our code more reusable (it is like an event).


To use it we have to defend the delegate outside the class.


![img](./delegate_1.PNG)


and we can use it in two way 

1. create it like a class and invoke it.



```
testDelegate test = new testDelegate();
 test(); //1
 test.invoke(); //2

```



2. pass it to a method.



![img](./delegate_2.PNG)


## json_format
![img](./json_format.PNG)


----
**[Learning Journal](./LearningJournal.md)**

---

**[← Back to LTUC Index](../ReadMeLTUC.md)**