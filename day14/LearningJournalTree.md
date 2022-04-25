# Tree :palm_tree:

so today we take about the tree in coding and we take about there is a lot of different types of tree but today we talked about Traversals in trees 

- Depth First : there we call the node one by one from the leef 
    1. Pre-order: `root` > `left` > `right`.
  
    2. In-order: `left` > `root` > `right`.

    3. Post-order: `left` > `right` > `root`.

in the three way we do almost the same code but we change the order of lines.
```
    ALGORITHM preOrder(root) //Pre-order 
    OUTPUT <-- root.value //root

    if root.left is not Null
        preOrder(root.left) //left

    if root.right is not NULL
        preOrder(root.right) //right
```
- Breadth First : there we call the node level by level

```
ALGORITHM breadthFirst(root)

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while ! breadth.is_empty()
     node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```
when we add a node in this code we add in an empty place from top to down level by level.
```
time complexity: O(w) (w: largest width in the tree)
```