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

Is similar to a Queue, but in this case, every element inside the priority queue has a priority value associated with it. The priority of the elements in a priority queue determines the order in which elements are served. If in any case the elements have same priority, they are served in the same way as a normal Queue.

**When to use a Priority queue?**

- When you need to get the next element with most priority.
- When dealing with "next best" or "next worse" searches.

**Examples**

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


### Set

A set is a data structure that can store any number of unique values in any order you wish.

### Map

Are data structures that store key-value pairs.

### Linked list

A linked list is a linear data structure, in which the elements are not stored at contigous memory locations. The elements in a linked list are linked using pointers. Each element is called "Node", and each "Node" contains a data field and a reference (link) to the next node.

### Doubly Linked list

Is a Linked List but this one contains an extra pointer used to point a previous element in a Node.
