## **Enums** :open_file_folder:

---

is a spatial type of class that we use to store so the number in value and that number we want to deal with it in another time.

way to use first create enum class



```
enum AnimalWedth 
{
    Lion = 0,
    Shark = 1,
    Cat = 100,
    Dog = 200
}
```

- it all starts in **pascal case** 

- if i want the name we call just the name 

    Example:
    ```
AnimalWedth.Lion // anser is Lion
    ```

- if i want the number i should cast the name 
 Example:
    ```
    (int)AnimalWedth.Lion // anser is 0
    ```

## **Collection**  :paperclip: 
---
is a group of related objects we but it inside `<>` and we can use collection with many things

1. **index collection**
    - array
    ```
    int animal = new int[6];
    ```
    - list
    ```
   List<string> salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };
    ```
    

2. **many values collection**

    - hash map
    ```
     Hashtable animal = new Hashtable();
    ```
    - dictionary
    ```
    Dictionary<string, string> animal = new Dictionary<string, string>();
    ```


NOTE : the main deferant between `hash map` and  `dictionary` is hash value and key are both from object type but in dictionary we can select the data type.

3. **special collection**

    - stack  
    ```
     Stack<string> numbers = new Stack<string>();
    ```
    - queue  
    ```
     Queue<string> numbers = new Queue<string>();
    ```



-----
## [**Learning Journal**](./LearningJournal.md) 

