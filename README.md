# Aim:
To study and implement the Linked List data structure in C++.

# Tools Used:
Visual Studio Code

Any online C++ Compiler like [OnlineGDB]

# Theory
A Linked List is a linear data structure where each element (called a node) is connected via pointers rather than stored in contiguous memory locations (like arrays). Each node has two parts:

Data: Stores the actual value.

Pointer (Next): Stores the address of the next node in the list.

# Features of Linked List:

Memory is allocated dynamically at runtime.

It allows efficient insertion/deletion without shifting elements.

It does not waste memory like arrays (which are often oversized to prevent overflow).

Each node can be anywhere in memory; the links (pointers) maintain the sequence.

# Why Use Linked Lists Instead of Arrays?

Feature	Array	Linked List

Memory	Contiguous	Non-contiguous

Size	Fixed at compile-time	Dynamic (can grow/shrink at runtime)

Insertion/Deletion	Costly (involves shifting)	Efficient (just change pointers)

Access	Direct (O(1) via index)	Sequential (O(n) traversal)

# Types of Linked Lists:

Singly Linked List → Each node points to the next node only.

Doubly Linked List → Each node points to both its previous and next nodes.

Circular Linked List → The last node points back to the first node, forming a loop.

# Program 1 – Create a Single Node
# Algorithm:
    Start the program.
    
    Define a class Node with:
    
    Data (int val) and pointer (Node* next).
    Constructor initializes data and sets next = NULL.
    In main():
    
    Create a node using new Node(1).
    Print the node’s value and its pointer (next).
    End the program.

Theory:
This is the foundational step in working with linked lists. We learn to define a node and understand its structure. Each node contains data and a pointer to the next node, which is initially NULL because no other nodes exist yet.

Sample Output Explanation:
Node value: 1
Next value: 0
Node value: 1 → The data part of the node is 1.
Next value: 0 → 0 or NULL signifies that there is no next node.
This indicates that the node has been created successfully and is not connected to any other node.

# Program 2 – Link and Traverse Multiple Nodes
# Algorithm:
    Start the program.
    
    Define a class Node with data (char val) and pointer (Node* next).
    
    Create three nodes: 10, 20, and 30.
    
    Link them:
    
    n1->next = n2
    n2->next = n3
    n3->next = NULL
    Use a pointer temp to traverse from head (n1) until NULL.
    
    Print each node’s value during traversal.
    
    End the program.

Theory:
In this step, we link multiple nodes to form a basic chain (linked list). The list starts from the head (first node), and traversal means moving from one node to the next using the next pointer until the end (NULL) is reached.

Sample Output Explanation:
10
20
30
This means nodes were successfully linked: A → B → C → NULL.
The traversal loop accessed each node one by one and printed the data.
This output shows that traversal and linking have been implemented correctly.

# Program 3 – Insert Node at Head
# Algorithm:
    Start the program.
    
    Define a class Link with data and next pointer.
    
    Write insert_head(head, value) function:
    
    Create a new node.
    Set new_node->next = head.
    Update head = new_node.
    Write disp(head) function:
    
    Traverse list from head to NULL.
    Print each node’s value with "->".
    End with "NULL".
    In main():
    
    Initialize head = NULL.
    Insert 30 at head → display.
    Insert 32 at head → display.
    Insert 35 at head → display.
    End the program.

Theory:
Inserting at the head means that each new node becomes the first element in the list. The previously first node becomes the second, and so on. This is a very efficient operation because it does not require traversal—only pointer adjustments.

Step-by-Step Operation:

Insert 30 → List: 30->NULL

Insert 32 → List: 32->30->NULL

Insert 35 → List: 35->32->30->NULL

Sample Output Explanation:

30->NULL

32->30->NULL

35->32->30->NULL

Each new insertion appears at the beginning of the list.

Demonstrates how inserting at the head reorders the list to include the new node first.

# Key Learning Outcomes

Understand the internal structure of a node and how pointers link nodes.

Learn to create and link nodes to form a singly linked list.

Learn how to traverse the list to access all elements.

Perform efficient insertions at the head of the list.

Understand how NULL is used to mark the end of the list.

# Applications of Linked Lists

Linked Lists are widely used in real-world systems and data structure implementations:

Dynamic memory allocation in OS.

Stacks and Queues implementation.

Graphs (adjacency lists) and Hash Tables.

Undo/Redo operations in text editors.

Browser History and Media Playlists.

Navigation systems using Doubly Linked Lists.

# Advantages of Linked List

Dynamic Size: Grows and shrinks as needed.

Efficient Insertion/Deletion: No shifting like in arrays.

Efficient Memory Utilization: No unused memory blocks.

Flexible Memory Allocation: Works well in fragmented memory.

Foundation of Advanced Structures: Used in trees, graphs, hash maps, etc.

# Conclusion:
In this session, we understood the Linked List data structure's structure, behavior, and advantages. We explored:

Node creation
Linking nodes
Traversal of linked lists
Insertion at the head
By learning these fundamentals, we gain the ability to build more complex and efficient data structures. Linked lists are crucial for solving problems involving dynamic memory and are a stepping stone to mastering data structures in C++.
