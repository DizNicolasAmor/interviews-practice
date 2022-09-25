# DATA STRUCTURES

## TABLE OF CONTENTS

- [General](#general)
  - Stack
  - Queue
  - Priority Queue
  - Set
  - Map
  - Linked List
  - Doubly Linked List

<a name="general" />

## General

A *data structure* is a way of organizing data so it can be used effectively.

### Stack

Is a linear data structure that follows the principle of Last in First Out (LIFO). It means the last element inserted is the one that is be removed first. You can think it as a pile of plates on top of another. Possible operations could be:

1. Push
2. Pop
3. IsEmpty
4. IsFull
5. Peek (Get the value of the top element without removing it).

### Queue

Like stacks, are collection of elements. But unlike stacks, they follow the Fist in First Out (FIFO) principle. Elements added to the queue are pushed to the end, and only the element at the front of the queue is allowed to be removed.

### Priority Queue

It is similar to a Queue, except that each element has a certain priority. The priority determines the order in which elements are served. If in any case the elements have same priority, they are served in the same way as a normal Queue.

**When to use a Priority queue?**

- When you need to get the next element with most priority.
- When dealing with "next best" or "next worse" searches.

**Usage examples**

- Used in Minimum Spanning Tree (MST) algorithm.
- Used in Huffman coding (for lossless data compression).

**Complexity**

| OPERATION | COMPLEXITY  |
| --------- | ----------- |
| Peek      | 0 (1)       |
| Enqueue   | 0 (log n)   |
| Dequeue   | 0 (log n)   |
| Contains  | 0 (log n)   |
| Remove    | 0 (log n)   |

** How to achieve it?**

Using a HEAP: a semiordered tree-based data structure in which each parent is greater than its children.

** How to INSERT a new element?**

1. Push it at the end.
2. If it is greater than its father, swap then.
3. Repeat step 2 until necessary.

** How to FIND a PARENT?**

The relation is `Math.floor(index/2)`.

** How to FIND the CHILDREN?**

- Index of child #1:  `indexFather x 2`.
- Index of child #2: `indexFather x 2 + 1`.

** How to REMOVE an element?**

1. Swap the root with the last element and `pop()` it.
2. If the new orrt is smaller than its children, swap it with the greatest.
3. Repeat step 2 until necessary.

**Visual example**

```
    9
   /  \
  8    5
 / \  / \
7  2 3   4

const myArray = [9, 8, 5, 7, 2, 3, 4]
```

### Set

A set is a data structure that can store any number of unique values in any order you wish.

### Map

Are data structures that store key-value pairs.

### Linked list

A linked list is a linear data structure, in which the elements are not stored at contigous memory locations. The elements in a linked list are linked using pointers. Each element is called "Node", and each "Node" contains a data field and a reference (link) to the next node.

### Doubly Linked list

Is a Linked List but this one contains an extra pointer used to point a previous element in a Node.
