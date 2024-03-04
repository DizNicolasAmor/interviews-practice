# DATA STRUCTURES

## TABLE OF CONTENTS

- [BASIC](#BASIC)
  - 1 What is a data structure?
  - 2 What is the concept of time complexity?
  - 3 What is an Array?
  - 4 What is a Stack?
  - 5 What is a Queue?
  - 6 What is a Priority Queue?
  - 7 What is a Set?
  - 8 What is a Map?
  - 9 What is a Linked List?
  - 10 What is a Graph?
  - 11 What is a Hash Table?
- [INTERMEDIATE](#INTERMEDIATE)
  - 12 How does a Hash Table hashing help in data retrieval?
  - 13 What is depth-first search (DFS) algorithm?
  - 14 When would you use DFS?
  - 15 What is breadth-first search (BFS) algorithm?
  - 16 When would you use BFS?
  - 17 How to implement a stack using an array?
  - 18 How to implement a stack using a linked list?
  - 19 What is a heap?
  - 20 What is a trie data structure, and how is it used in string manipulation and search operations?
  - 21 What is dynamic programming?
  - 22 What is the difference between a Hash Table and an Array?
- [ADVANCED](#ADVANCED)
  - 23 How would you implement a simple sorting algorithm?
  - 24 Can you describe the basic principles of recursion?
  - 25 How do you detect cycles in a directed graph?
  - 26 What is a balanced binary search tree?
  - 27 What are the principles of divide and conquer algorithms?
  - 28 What are persistent data structures?
  - 29 What is a suffix tree?
  - 30 What is a segment tree and its applications?
  - 31 How do you implement a trie data structure efficiently?
  - 32 What are bloom filters and how do they work?
  - 33 What is a disjoint-set data structure?

<a name="BASIC" />

## BASIC

### 1 What is a data structure?

A *Data Structure* is a way of organizing data so it can be used effectively.

An *Abstract Data Structure* is an abstraction of the DS which provides only its interface, that is without the details of the implementation. Examples: Stack, Queue, List, Tree, Graph, Map, Set, Multiset, Container, Array.

### 2 What is the concept of time complexity?

- It refers to the measure of the amount of time an algorithm takes to complete as a function of the size of its input.
- It quantifies the efficiency of an algorithm by analyzing how its runtime scales with increasing input size.
- It is typically expressed using `Big O notation`.
- It helps in comparing algorithms and predicting their performance under different scenarios.

### 3 What is an Array?

**Static Array**: it is a fixed length container of indexable elements that starts from index zero. Each index could be referenced with a number.

**Dynamic Array**: it is a dynamic length container of indexable elements that starts from index zero. Each index could be referenced with a number.

**Complexity**

| OPERATION | STATIC ARRAY | DYNAMIC ARRAY |
| --------- | ------------ | ------------- |
| Access    | 0 (1)        | 0 (1)         |
| Search    | 0 (n)        | 0 (n)         |
| Insert    | N / A        | 0 (n)         |
| Append    | N / A        | 0 (1)         |
| Remove    | N / A        | 0 (n)         |

### 4 What is a Stack?

It is a linear data structure that models a real world stack. It follows the principle of Last in First Out (LIFO): that means the last element inserted is the one that is be removed first. You can think it as a pile of plates on top of another.

**Operations**

1. `Push`: add an element.
2. `Pop`: remove an element.
3. `Search`: search for an element.
4. `Size`: get the quantity of elements in the stack.
5. `IsEmpty`: if size = 0.
6. `Peek`: get the top value without removing it.

**Usage examples**

- Undo mechanisms in text editors.
- Browser history.

**Complexity**

| OPERATION | Complexity |
| --------- | ---------- |
| Push      | 0 (1)      |
| Pop       | 0 (1)      |
| Peek      | 0 (1)      |
| Search    | 0 (n)      |
| Size      | 0 (1)      |

### 5 What is a Queue?

It is a linear data structure that models a real world queue. It follows the Fist in First Out (FIFO) principle. Elements added to the queue are pushed to the end, and only the element at the front of the queue is allowed to be removed. Those operations are called `enqueue` and `dequeue`.

**Usage examples**

- Waiting lives. For example, the queue of files to download.

**Complexity**

| OPERATION | Complexity |
| --------- | ---------- |
| Enqueue   | 0 (1)      |
| Dequeue   | 0 (1)      |
| Peek      | 0 (1)      |
| Contains  | 0 (n)      |
| Remove    | 0 (n)      |
| Size      | 0 (1)      |

### 6 What is a Priority Queue?

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

**How to achieve it?**

Using a HEAP: a semiordered tree-based data structure in which each parent is greater than its children.

**How to INSERT a new element?**

1. Push it at the end.
2. If it is greater than its father, swap then.
3. Repeat step 2 until necessary.

**How to FIND a PARENT?**

The relation is `Math.floor(index/2)`.

**How to FIND the CHILDREN?**

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

### 7 What is a Set?

A set is a data structure that can store any number of unique values in any order you wish.

### 8 What is a Map?

Are data structures that store key-value pairs.

### 9 What is a Linked List?

A linked list is a linear data structure, in which the elements are not stored at contigous memory locations. The elements in a linked list are linked using pointers. Each element is called "Node", and each "Node" contains a data field and a reference (link) to the next node.

**Some implementations**

- Simple Linked List: this one contains only one pointer to the next node.
- Double Linked List: this one contains an extra pointer to the previous node.
- Circular Linked List: this one contains extra pointers in the first and last nodes to connect each other.
- Circular Double List: the name is very explicit.

**Terminology**

- `node`: object containing data and a pointer.
- `pointer`: the reference to another node or null.
- `head`: the first node.
- `tail`: the last node.

**Complexity**

| OPERATION        | Single LL  | Double LL  |
| ---------------- | ---------- | ---------- |
| Search           | 0 (n)      | 0 (n)      |
| Insert at head   | 0 (1)      | 0 (1)      |
| Insert at tail   | 0 (1)      | 0 (1)      |
| Remove from head | 0 (1)      | 0 (1)      |
| Remove from tail | 0 (n)      | 0 (1)      |
| Remove in middle | 0 (n)      | 0 (n)      |

### 10 What is a Graph?

It is a data structure composed of nodes (vertices) and edges that connect pairs of nodes. Graphs are used to represent relationships or connections between objects, with nodes representing entities and edges representing the relationships between them.

### 11 What is a Hash Table?

It is a data structure that stores key-value pairs, allowing for efficient lookup, insertion, and deletion operations. It uses a hash function to map keys to indices in an array, enabling constant-time access to values associated with keys.

<a name="INTERMEDIATE" />

## INTERMEDIATE

### 12 How does a Hash Table hashing help in data retrieval?

Hash tables use hashing to map keys to indices in an array, providing constant-time access to values associated with keys. The hash function converts the key into a hash code, which determines the index where the value is stored. This enables efficient data retrieval as it eliminates the need for sequential search and allows direct access to stored values based on their keys. However, collisions can occur when two keys hash to the same index, which must be resolved using collision resolution techniques such as chaining or open addressing.

### 13 What is depth-first search (DFS) algorithm?

Depth-first search (DFS) is an algorithm used to traverse or search tree or graph data structures. It starts at a designated node and explores as far as possible along each branch before backtracking. This approach can be implemented recursively or iteratively using a stack. DFS is often used in maze solving, topological sorting, and graph traversal problems.

### 14 When would you use DFS?

- Graph Traversal.
- Path Finding: searching for a path between two nodes in a graph.
- Topological Sorting: using it on a directed acyclic graph (DAG).
- Maze Solving: exploring all possible paths until you find a solution.
- Detecting Cycles: detecting cycles in a graph, which is essential in tasks like deadlock detection or cycle detection in resource allocation systems.

### 15 What is breadth-first search (BFS) algorithm?

It is an algorithm used to traverse or search tree or graph data structures. It starts at a designated node and explores all neighbor nodes at the current depth before moving to the next depth level. This approach is implemented using a queue data structure and ensures that nodes are visited in increasing order of distance from the starting node.

### 16 When would you use BFS?

BFS is often used in finding the shortest path, network analysis, and puzzle-solving problems.

### 17 How to implement a stack using an array?

- Maintaining a pointer to the top of the stack.
- Using array indices to represent stack elements.
- "Push" operations involve incrementing the pointer and placing the new element at the top of the stack.
- "Pop" operations decrement the pointer to remove the top element.
- "Stack overflow" and "Stack underflow" should be considered by checking the stack size and pointer position.

### 18 How to implement a stack using a linked list?

complete

### 19 What is a heap?

complete

### 20 What is a trie data structure, and how is it used in string manipulation and search operations?

complete

### 21 What is dynamic programming?

complete

### 22 What is the difference between a Hash Table and an Array?

complete

<a name="ADVANCED" />

## ADVANCED

### 23 How would you implement a simple sorting algorithm?

complete

### 24 Can you describe the basic principles of recursion?

complete

### 25 How do you detect cycles in a directed graph?

complete

### 26 What is a balanced binary search tree?

complete

### 27 What are the principles of divide and conquer algorithms?

complete

### 28 What are persistent data structures?

complete

### 29 What is a suffix tree?

complete

### 30 What is a segment tree and its applications?

complete

### 31 How do you implement a trie data structure efficiently?

complete

### 32 What are bloom filters and how do they work?

Bloom filters are probabilistic data structures used to test whether an element is a member of a set. They work by hashing elements into a bit array of fixed size, typically setting multiple bits per element. When checking for membership, the filter hashes the element and checks if the corresponding bits are set. False positives are possible, but false negatives are not. Bloom filters are space-efficient and offer constant-time lookups, making them useful for applications like spell checking, caching, and network routing.

### 33 What is a disjoint-set data structure?

A disjoint-set data structure, also known as a union-find data structure, is used to maintain a collection of disjoint sets. It supports two main operations: union, which merges two sets into one, and find, which determines which set a particular element belongs to. They are often used in algorithms for graph connectivity problems, such as determining whether two nodes are connected in a graph or finding minimum spanning trees.
