# .Net

**_SpeedTest_**

---

```C#
Stopwatch s = new Stopwatch();

s.Start/s.Stop/s.ElapsedMillseconds
```

---

**_PriorityQueue_**

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
