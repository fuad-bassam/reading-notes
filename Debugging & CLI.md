

##
 ```
 Database
```

**Relational Database?**: A database the data inside it organized and sorted into tables 

**SQL** : (Structured Query Language) a programming language used to communicate with relational data and do  processes on data like

- SELECT data  `SELECT colome-name FROM Data-base ;` and add some conditions in the last like
    1. WHERE  
    2. LIKE "%WALL%"
    3. LIMIT 3
    4. 
- INSERT data `INSERT INTO table-name (column-name, ..) VALUES (data, ..);` 
- DELETE data `DELETE FROM table-name WHERE any-thing;`
- UPDATE data `UPDATE table_name SET column =  data ;
- CREATE tables `CREATE TABLE table-name ( column-name TEXT, ..);` and in scema use 
    
    DROP TABLE table-name;
    CREATE TABLE IF NOT EXISTS table-name ....

    ![image](https://firebasestorage.googleapis.com/v0/b/f22f-3c23f.appspot.com/o/DotNet%2Fre-sql.PNG?alt=media&token=6b663722-be06-4cb6-a293-7e3f79b76baa)

    ![image](https://firebasestorage.googleapis.com/v0/b/f22f-3c23f.appspot.com/o/DotNet%2Fre-sql-2.PNG?alt=media&token=6d5f88ae-a354-4f7c-9685-286a5f30de8b)

    ![image](https://firebasestorage.googleapis.com/v0/b/f22f-3c23f.appspot.com/o/DotNet%2Fre-sql-3.PNG?alt=media&token=d36d223c-03ba-497d-8d5f-4ac8d94063b0)


##
 ```
CLI
```
**CLI** : (Command-line interface) text interface this text called command and there is type of command
the command line inside any OS can fined it (Linux , Windows ,...)

- Navigation command like .
    1. `pwd` : to get the path for your location .
    2. `cd +path` : to go inside the directory .
    3. `cd ..` : to go outside the directory by one step .
    4. `ls`: to get all the files in the directory that i am inside it .

- File Manipulation .
   1. `mkdir` : to creat directory . 
   2. `rmdir` : delete directory .
   3. `touch` : to creat file .
   4. `cp` : copy data form file to file .
   5. `mv` : delete file .


**some tips in CLI**
 
 - key 'Q' to exit page or stop . 
- key 'TAB' to auto complete the statement .

-----


## ``` Debugging & Exception Handling ```

Debugging: the way that we use to find the problem in our code by running the code step by step.

we can debug our code in some platform like `Visual Studio`.

in visual studio we can debug our code and see the running steps and pause it in these steps.

 1. ![select Debug button for the menu bar](https://firebasestorage.googleapis.com/v0/b/f22f-3c23f.appspot.com/o/re-erorr1.PNG?alt=media&token=2c48de22-8e3a-4d26-8d4f-2a37c47dc539) 
 2. ![press Start Debugging](https://firebasestorage.googleapis.com/v0/b/f22f-3c23f.appspot.com/o/re-erorr2.PNG?alt=media&token=5f766765-e09e-479b-bff7-8b2758a1871f) 

 **or by using `F5`**

 ```
 TIPS

when debugging is run you can put some code to show the expected valve or what happened like (`Console.WriteLine()`)
OR if i hilite the variable that will give my the value inside it now.
```
---
we can also handle some problems in CLR (Common Language Runtime) by using statement called  `try/catch` there `throw` ,`try-catch-finally` ,....

like in try/catch work by but the code that you think can make the problem inside try curly brackets and how i should handle this problem inside catch curly brackets.

----------------------