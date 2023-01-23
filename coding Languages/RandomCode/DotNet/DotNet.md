# .Net

## **_SpeedTest_**

---

```C#
Stopwatch s = new Stopwatch();

s.Start/s.Stop/s.ElapsedMillseconds
```

---

## **_PriorityQueue_**

---

```C#
    //Notes
    //1. it work on .net 6 and above
    //2. by default it minHeap to make it maxHeap we need to add "Comparer" 
    //or when we enqueue the node make the negative value
    //Like   "pq.Enqueue(k.Key, k.Value);" =>"pq.Enqueue(kvp.Key, -kvp.Value);"

    //MaxHeap
    var queue = new PriorityQueue<int,int>(Comparer<int>.Create((x,y)=>y-x));

    //MaxMin
    var queue = new PriorityQueue<int,int>();
```

```C#
    // for more custom comparer
    public class NameComparer: IComparer<KeyValuePair<string, int>>
{
  public int Compare(KeyValuePair<string, int> x, KeyValuePair<string,int> y) => 
  (x.Value == y.Value) ? (x.Key.CompareTo(y.Key)) : (y.Value-x.Value);
} 
```

---

## **_nested arrays_**

---

```C#
// there is two types of nested arrays 
//1 int[,] in This type all rows in the array have the same number of columns.

//declare array 
int[,] array = new int[3, 4];
//get length x and y
 array.GetLength(0);//x
 array.GetLength(1);//y

//2 int[][] in This type each row in the array can have a different number of columns.

//declare array 

int[][] array = new int[3][];
array[0] = new int[4];
array[1] = new int[5];
array[2] = new int[6];

//get length x and y
 array.Length;//x
 array[0].Length;//y
```

---
