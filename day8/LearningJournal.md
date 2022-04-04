## emums :open_file_folder:

is a spatial type of class that we use to store in its variables containing numbers.

in **emuns** we can call just the name if we want the name of the element 

   
    `AnimalWedth.Lion() // Anser is Lion`
  
**OR** we can cast it to get the number (the value) inside the name 

    `(int)AnimalWedth.Lion // anser is like 5 or any number inside Lion ` 





NOTE:  
any class that didn't inherit anther class that inherit objct class.
that mean that we can override `ToString()` , `Equals()`, `GetHashCode()`.

## Collection :paperclip: 

there are two types of Collection 

1. generic it is deal with one type of data (the first type of data we send it) 

    - `<string>` , `<int>` ,`<T>` we use it for not specific data type form the first, it takes his value when we add element. 



 Some cllection 
-----------


- List
    we can create list in many way.
    - `List<string> numbersStrLst = new List<string>(); // initialize` 
          
    - `List<string> numbersStrLst = new List<string>{ "One", "Two", "Three"}; //initialize and add element`


    to get list length we not use **.Length** we use **.Count**.

- dictionary 
    is a group of hash data but we declare data type for `key and value`.

    inside dictionary we usualy deal with data as `KeyValuePair` it have inside it **.Key** & **.Value** to get the data .

    if we add data have the same **key** that one of the elements had it make an `Error`.    
    

2. non-generic it is deal with more than one data types.

