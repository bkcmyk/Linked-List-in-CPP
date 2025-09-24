
# LINKED LIST IN C++

**Aim:**
To study and implement the **Linked List** data structure in C++.

**Tools Used:**

* VS Code or any online C++ Compiler

---

## Theory

A **Linked List** is a linear data structure in which elements are connected using pointers instead of being stored in contiguous memory locations like arrays. Each element in the linked list is called a **node**, and it contains:

* **Data** → the value stored in the node.
* **Pointer (next)** → address of the next node in the sequence.

Thus, nodes are dynamically linked together to form a chain.

<img width="957" height="189" alt="image" src="https://github.com/user-attachments/assets/4027c904-3621-4480-a7bf-a49c348ae5ef" />


### Why Linked List?

1. **Dynamic Size:** Memory is allocated or deallocated at runtime.
2. **Ease of Insertion/Deletion:** Unlike arrays, no shifting of elements is needed.
3. **Efficient Memory Utilization:** Uses only as much memory as required.
4. **Implementation Basis:** Advanced data structures like stack, queue, graphs, and hash maps are built using linked lists.

### General Syntax of a Linked List Node

```cpp
class Node {
public:
    int data;     // data stored in node
    Node* next;   // pointer to next node

    Node(int value) {
        data = value;
        next = NULL;
    }
};
```

Here:

* `data` stores the node’s value.
* `next` stores the pointer to the next node.
* Constructor initializes the node with given data and sets `next = NULL`.

### Types of Linked Lists

1. **Singly Linked List:** Each node points to the next node.
2. **Doubly Linked List:** Each node points to both previous and next nodes.
3. **Circular Linked List:** The last node points back to the first node.

---

## Program 1 – Create a Single Node

**Algorithm:**

1. Start the program.
2. Define a class `Node` with:

   * Data (`int val`) and pointer (`Node* next`).
   * Constructor initializes data and sets `next = NULL`.
3. In `main()`:

   * Create a node using `new Node(1)`.
   * Print the node’s value and its pointer (`next`).
4. End the program.

**Sample Output:**

```
Node value: 1
Next value: 0
```

---

## Program 2 – Link and Traverse Multiple Nodes

**Algorithm:**

1. Start the program.
2. Define a class `Node` with data (`char val`) and pointer (`Node* next`).
3. Create three nodes: `A`, `B`, and `C`.
4. Link them:

   * `n1->next = n2`
   * `n2->next = n3`
   * `n3->next = NULL`
5. Use a pointer `temp` to traverse from head (`n1`) until `NULL`.
6. Print each node’s value during traversal.
7. End the program.

**Sample Output:**

```
A
B
C
```

---

## Program 3 – Insert Node at Head

**Algorithm:**

1. Start the program.
2. Define a class `Link` with data and next pointer.
3. Write `insert_head(head, value)` function:

   * Create a new node.
   * Set `new_node->next = head`.
   * Update `head = new_node`.
4. Write `disp(head)` function:

   * Traverse list from head to `NULL`.
   * Print each node’s value with `"->"`.
   * End with `"NULL"`.
5. In `main()`:

   * Initialize `head = NULL`.
   * Insert 30 at head → display.
   * Insert 32 at head → display.
   * Insert 35 at head → display.
6. End the program.

**Sample Output:**

```
30->NULL
32->30->NULL
35->32->30->NULL
```

---

## Key Learning Outcomes

* Learn how to **create a node dynamically** using constructors.
* Understand how nodes are linked together in a chain.
* Implement **traversal** to display linked list contents.
* Perform **insertion at the head** of a linked list.
* Understand that `NULL` indicates the end of the list.

---

## Applications of Linked List

* **Dynamic Memory Management** in operating systems.
* **Stacks and Queues** implementation.
* **Graphs and Hash Tables** structures.
* **Undo/Redo** in text editors.
* **Playlists** in music or video players.
* **Navigation Systems** (using doubly linked lists).

---

## Advantages

* Size is not fixed → grows or shrinks dynamically.
* Insertion and deletion are faster compared to arrays.
* Efficient use of memory.
* Forms the foundation of many advanced data structures.
