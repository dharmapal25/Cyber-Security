![alt text](image.png)
✅ **ARRAYS (1D, 2D, 3D) – EXAM SHORT NOTES**



**1. Definition (Two lines)**

An array is a collection of elements of the **same data type**, stored in **continuous memory locations**.
It helps to store multiple values under **one single variable name**.

---

**2. Example**

```c
int marks[5] = {10, 20, 30, 40, 50};


✅ **3. Types of Arrays**

1. **One-Dimensional Array (1D)**
2. **Two-Dimensional Array (2D)**
3. **Three-Dimensional Array (3D)**

# ⭐ **1D ARRAY**

### **Definition**

A one-dimensional array is a linear list of elements stored in a single row.

**3 Points

* Stores data in a straight line (single row).
* Accessed using **one index**.
* Memory is allocated **sequentially**.

Syntax
data_type array_name[size];


### **Example**

int arr[4] = {1, 2, 3, 4};


# ⭐ **2D ARRAY**

### **Definition**

A two-dimensional array is a combination of rows and columns, also called a **matrix**.

3 Points

* Represented in **rows and columns**.
* Accessed using **two indexes**.
* Used to store table-like data.

Syntax
data_type array_name[rows][columns];

Example
int matrix[2][3] = {
  {1, 2, 3},
  {4, 5, 6}
};


# ⭐ **3D ARRAY**

Definition
A three-dimensional array is an array of 2D arrays, like storing multiple matrices.

**3 Points**
* Represented as **blocks of 2D arrays**.
* Accessed using **three indexes**.
* Used in graphics, simulations, 3D data.

Syntax
data_type array_name[x][y][z];

Example
int cube[2][2][2] = {
  {{1,2}, {3,4}},
  {{5,6}, {7,8}}
};


ARRAY ADVANTAGES (6 POINTS)
1. Easy to access elements using index.
2. Fast searching and traversal.
3. Stores multiple values under one variable name.
4. Memory-efficient due to continuous allocation.
5. Easy to implement mathematical operations.
6. Used to create advanced data structures (stack, queue, matrix).


# 📌 **Representation of Arrays in Memory (IMPORTANT)**

Array elements are stored in **continuous memory**.
Index → address calculated using a formula.

---

# ⭐ **CMO (Column Major Order)**

* Columns are stored **first**, then rows.
* Used in **Fortran, MATLAB**.
* Useful for mathematical and matrix calculations.


2D Array Example
Matrix:
| a00 | a01 | a02 |
| a10 | a11 | a12 |

CMO memory order:
a00, a10, a01, a11, a02, a12

⭐ **RMO (Row Major Order)**

* Rows are stored **first**, then columns.
* Used in **C, C++, Java**.
* Faster for row-wise operations.

RMO memory order:**
a00, a01, a02, a10, a11, a12


⭐ Formula (Important for exams)
For RMO (C Language)
Address = Base + [ (i * total_columns) + j ] * size

For CMO
Address = Base + [ (j * total_rows) + i ] * size

----------------------------------------


✅ **Sparse Matrix Representation & Advantages**

1. Definition (Two lines)**

A sparse matrix is a matrix in which **most of the elements are zero**.
It stores only **non-zero values** to save memory and increase efficiency.

---

**2. Example**

Matrix (5×5) with only 4 non-zero values:

|0 |0 |3 |0 |0|
|0 |0 |0 |0 |0|
|4 |0 |0 |0 |0|
|0 |0 |0 |5 |0|
|0 |0 |0 |0 |9|

Non-zero values = 4 → Sparse Matrix


3. Why Sparse Matrix is Used (Three lines)**

Sparse matrices reduce **memory usage** because only non-zero values are stored.
They make operations **faster** for large datasets like graphs or networks.
They avoid storing unnecessary zeros, which saves **space and processing time**.


⭐ 4. Sparse Matrix Representation (3-tuple form)

Stored as:
(Row, Column, Value)

Example for the above matrix:

| Row | Col | Value |
| --- | --- | ----- |
| 0   | 2   | 3     |
| 2   | 0   | 4     |
| 3   | 3   | 5     |
| 4   | 4   | 9     |

This is called the **Triplet Representation** (or 3-tuple).


5. Computing Time (Sparse Matrix) – 2 lines

Sparse matrices reduce computing time because algorithms process **only non-zero elements**.
This avoids unnecessary operations on zero values, making computation faster.


✅ Advantages of Sparse Matrix (6 Points)

1. Saves Memory
Only non-zero elements are stored, reducing memory usage.

2. Faster Processing
Computations are performed only on non-zero values, improving speed.

3. Efficient Storage Structure
Uses compact formats like 3-tuple or linked list, avoiding storage of zeros.

3. Improves Algorithm Performance
Useful in problems like graphs, networks, and scientific data where zeros are common.

4. Reduced I/O Operations
Less data to read/write because zeros are not stored.

5. Better for Large Matrices
Especially beneficial when matrix size is huge but non-zero values are very few.


--------------


✅ SINGLY LINKED LIST: INSERTION & DELETION
1. Definition + 2 Points

* A singly linked list is a linear data structure in which elements (nodes) are connected using pointers.
* Each node contains data and a pointer to the next node.
* The last node points to NULL, indicating the end of the list.

2. Example (Singly Linked List)
Head -> [10|Next] -> [20|Next] -> [30|Next] -> NULL

✅ 3. INSERTION OPERATION
Definition
Insertion in a singly linked list means adding a new node at a specific position (beginning, end, or middle).

Algorithms

a) Insertion at Beginning
* Create a new node.
* Set new node’s next to head.
* Update head to new node.

Example/Diagram
Before: Head -> 10 -> 20 -> NULL
Insert 5 at beginning:
After: Head -> 5 -> 10 -> 20 -> NULL

b) Insertion at End
* Create a new node.
* Traverse to the last node.
* Set last node’s next to new node.

Example/Diagram
Before: Head -> 10 -> 20 -> NULL
Insert 30 at end:
After: Head -> 10 -> 20 -> 30 -> NULL

✅ 4. DELETION OPERATION

Definition
Deletion in a singly linked list means removing a node from beginning, end, or a specific position.

Algorithms
a) Deletion at Beginning
* Store head in temp.
* Move head to next node.
* Delete temp.

Example/Diagram
Before: Head -> 10 -> 20 -> 30 -> NULL
Delete beginning:
After: Head -> 20 -> 30 -> NULL


b) Deletion at End
* Traverse to the second last node.
* Set its next to NULL.
* Delete last node.

Example/Diagram
Before: Head -> 10 -> 20 -> 30 -> NULL
Delete end:
After: Head -> 10 -> 20 -> NULL


----------

Array vs Linked List ke comparison table


-----------

✅ Polynomial Addition Using Linked List
1. Definition (Two lines)

Polynomial addition using linked list is the process of adding two polynomials where each term is represented as a node in a linked list.
Each node contains coefficient and exponent of the term.

2. Example

Polynomial 1: 
5
𝑥
3
+
4
𝑥
2
+
2
5x
3
+4x
2
+2
Polynomial 2: 
3
𝑥
3
+
2
𝑥
+
1
3x
3
+2x+1

Result: 
(
5
+
3
)
𝑥
3
+
4
𝑥
2
+
2
𝑥
+
(
2
+
1
)
=
8
𝑥
3
+
4
𝑥
2
+
2
𝑥
+
3
(5+3)x
3
+4x
2
+2x+(2+1)=8x
3
+4x
2
+2x+3

3. Why Linked List is Used

Polynomials can have different number of terms → dynamic size is required.

Insertion/deletion of terms is efficient using pointers.

Avoids wasting memory for zero-coefficients.

4. Representation Using Linked List

Each node contains:

coeff → Coefficient of term

pow → Exponent of term

next → Pointer to next node

Example (Polynomial 
Example (Polynomial 
5𝑥3+4𝑥2+25x3+4x2+2):

Head -> [5|3|Next] -> [4|2|Next] -> [2|0|Next] -> NULL

5. Algorithm for Polynomial Addition

Step 1: Initialize two linked lists poly1 and poly2.
Step 2: Compare exponents of current nodes of both lists.
* If poly1.exp > poly2.exp: Copy poly1 node to result and move poly1 to next.
* If poly1.exp < poly2.exp: Copy poly2 node to result and move poly2 to next.
* If poly1.exp == poly2.exp: Add coefficients, create new node with sum and exponent, move both pointers.
Step 3: Append remaining nodes from either list.
Step 4: Result is the sum polynomial linked list.

7. Advantages of Using Linked List for Polynomial
* Dynamic size → efficient memory usage.
* Easy insertion/deletion of terms.
* Handles polynomials with large gaps in exponents efficiently.

------------

✅ TREES – EXAM SHORT NOTES

1. Definition (Two lines)
-> A tree is a non-linear hierarchical data structure consisting of nodes connected by edges.
It has a root node and zero or more child nodes, forming parent-child relationships.

2. Example
       10
      /  \
     20   30
    / \
   40 50
  
  This is a simple tree with root 10.

✅ 3. Basic Terms in Tree

- Root Node
The topmost node of the tree from which all nodes descend.
Example: In above tree, root = 10.

- Edge
A connection between two nodes (parent to child).
Example: Edge between 10 → 20.

- Leaf Node
Nodes without any children.
Example: 40, 50, 30.

- Level
The distance of a node from the root (root at level 0).
Example: Level of 10=0, 20=1, 40=2.

- Siblings
Nodes having the same parent.
Example: 40 & 50 are siblings.

- Path
Sequence of nodes from one node to another.
Example: Path from 10 to 50 = 10 → 20 → 50.

- Subtree
A tree formed from any node and its descendants.
Example: Subtree rooted at 20 = 20 → 40 → 50.

- Degree of Node
Number of children of a node.
Example: Degree of 10=2, 20=2, 40=0.

- Height of Node
Number of edges on the longest path from node to a leaf.
Example: Height of 20=1, 10=2.

- Depth of Node
Number of edges from root to that node.
Example: Depth of 50=2, 30=1.

✅ 4. Trees Properties
👉 Every tree has one root and zero or more subtrees.
👉 Number of edges = Number of nodes – 1.
👉 Maximum nodes at level i = 2^i (for binary tree).
👉 Maximum number of nodes in a tree of height h = 2^(h+1) - 1 (binary tree).
👉 Height of a tree with n nodes ≥ log2(n+1) (minimum height).

------------

✅ TYPES OF BINARY TREES
1. Definition (Two lines)

A binary tree is a tree in which each node has at most two children (left and right).
It is widely used in searching and sorting algorithms.

2. Example
       10
      /  \
     20   30
    / \
   40  50

This is a binary tree with root 10.

✅ 3. Types of Binary Trees
a) Strict (Proper / Full) Binary Tree

Definition (2 lines):
A strict binary tree is a tree where every node has either 0 or 2 children.
No node has only one child.

Points:
👉 Every internal node has exactly 2 children.
👉 Leaf nodes have 0 children.

Example:

       1
      / \
     2   3
    / \
   4   5

b) Complete Binary Tree

Definition (2 lines):
A complete binary tree is completely filled on all levels except possibly the last, which is filled from left to right.

Points:
👉 Nodes are filled level by level.
👉 Last level may not be full, but left-aligned.

Example:

       1
      / \
     2   3
    / \
   4   5

c) Perfect Binary Tree

Definition (2 lines):
A perfect binary tree is both full and complete.
All internal nodes have 2 children, and all leaf nodes are at the same level.

Points:
👉 Maximum nodes possible at all levels.
👉 Number of nodes = 2^(height+1) - 1

Example:

       1
      / \
     2   3
    / \  / \
   4  5 6  7

d) Balanced Binary Tree

Definition (2 lines):
A balanced binary tree has minimum height possible.
The difference between the heights of left and right subtrees of any node is ≤1.

Points:
👉 Improves search performance.
👉 Avoids skewed tree structure.

Example:

       10
      /  \
     5    15
    / \
   2   7

e) Extended (Threaded) Binary Tree

Definition (2 lines):
An extended binary tree is a tree where all null pointers are replaced with special nodes or threads.
It helps efficient in-order traversal without recursion or stack.

Points:
👉 Uses “threads” to point to in-order predecessor/successor.
👉 Reduces memory and time in traversal.

Example (conceptual):

       10
      /  \
     5    15
   (threads connect null pointers to inorder neighbors)


---------

✅ TREE TRAVERSAL TECHNIQUES
1. Definition (Two lines)

Tree traversal is the process of visiting all nodes of a tree in a specific order.
It is used to search, display, or process nodes of a tree.

✅ 2. Types of Tree Traversal
a) Inorder Traversal

Definition (2 lines):
In Inorder traversal, nodes are visited in the order: Left → Root → Right.
It is mainly used to get sorted order of elements in a binary search tree (BST).

Example:
Binary Tree:

       10
      /  \
     5    20

Inorder: 5 → 10 → 20

b) Preorder Traversal

Definition (2 lines):
In Preorder traversal, nodes are visited in the order: Root → Left → Right.
It is used to create a copy of the tree or expression tree evaluation.

Example:
Binary Tree:

       10
      /  \
     5    20

Preorder: 10 → 5 → 20

c) Postorder Traversal

Definition (2 lines):
In Postorder traversal, nodes are visited in the order: Left → Right → Root.
It is used to delete the tree or evaluate postfix expressions.

Example:
Binary Tree:

       10
      /  \
     5    20

Postorder: 5 → 20 → 10


----------


✅ Construct Binary Tree Using Inorder + Preorder Traversal
1. Definition (Two lines)

Constructing a binary tree using inorder and preorder traversal means building the original tree structure when the inorder and preorder sequences are given.
It is widely used in tree reconstruction and expression trees.

2. Example
Given:

Preorder: A B D E C F
Inorder: D B E A F C

Constructed Tree:

       A
      / \
     B   C
    / \   \
   D   E   F

3. Algorithm (Step-wise, 1 line each)

1. Pick the first element of preorder as root.
2. Find the root index in inorder sequence.
3. Elements to the left of root in inorder → left subtree.
4. Elements to the right of root in inorder → right subtree.
5. Recursively repeat steps 1–4 for left and right subtrees.
6. Stop recursion when subtree has no elements.

Key Point:
👉 Preorder gives root nodes in order.
👉 Inorder gives left and right subtree structure.


--------


✅ Construct Binary Tree Using Inorder + Postorder Traversal
1. Definition (Two lines)

Constructing a binary tree using inorder and postorder traversal means building the original tree when inorder and postorder sequences are given.
It is commonly used in tree reconstruction and expression trees.

2. Example
Given:

Postorder: D E B F C A
Inorder: D B E A F C

Constructed Tree:

       A
      / \
     B   C
    / \   \
   D   E   F

3. Algorithm (Step-wise, 1 line each)

1. Pick the last element of postorder as root.
2. Find the root index in inorder sequence.
3. Elements to the left of root in inorder → left subtree.
4. Elements to the right of root in inorder → right subtree.
5. Recursively repeat steps 1–4 for left and right subtrees.
6. Stop recursion when subtree has no elements.

Key Point:
👉 Postorder gives root nodes in reverse order (last element is root).
👉 Inorder gives left and right subtree structure.


---------


1. Definition (Two lines)

A Binary Search Tree (BST) is a binary tree in which for every node, all elements in the left subtree are smaller and all elements in the right subtree are greater.
It is mainly used for fast searching, insertion, and deletion.

2. Example

General Tree:

       10
      /  \
     20   30


Binary Tree:

       10
      /  \
     5    15


Binary Search Tree (BST):

       10
      /  \
     5    15
    / \    \
   2   7    20


3. Operations (5 points, full lines)

Insertion:
Start from root, compare value, move left/right accordingly, insert node at empty position to maintain BST property.

Searching:
Start from root, compare key with current node, go left if smaller, right if greater, repeat until key found or NULL.

Deletion:
Case 1: Node is leaf → remove directly.
Case 2: Node has one child → link parent to child.
Case 3: Node has two children → replace with inorder predecessor or successor and delete that node.

Traversal:
Inorder traversal of BST gives sorted order of elements.

Height of BST:
Determines efficiency: minimum height → operations fast; skewed BST → operations slow.

4. Advantages of BST (4 points)
👉 Efficient search, insertion, deletion – average O(log n).
👉 Maintains sorted order via inorder traversal.
👉 Dynamic memory allocation – nodes can grow/shrink.
👉 Used in applications like database indexing, priority queues, and maps.

5. Disadvantages of BST
👉 Performance depends on tree height – skewed tree is inefficient (O(n)).
👉 Requires balanced tree maintenance for consistent performance.
👉 More complex than simple arrays for small datasets.


-------------


✅ Binary Search Tree (BST) – Operations
1. Insertion in BST

Definition:
Insertion means adding a new node to BST while maintaining the BST property (left < root < right).

Algorithm Steps (Simple):

1. Start at root.
2. Compare new value with current node.
3. If new value < current node → move left; else move right.
4. Repeat until an empty spot is found.
5. Insert the new node there.

Example: Insert 12 into BST:

      15
     /  \
    10   20

→ After insertion:

      15
     /  \
    10   20
      \
      12

2. Searching in BST

Definition:
Searching means finding whether a given value exists in the BST.

Algorithm Steps (Simple):

1. Start at root.
2. Compare key with current node.
3. If key = node → found, stop.
4. If key < node → move left, else move right.
5. Repeat until node found or NULL.

Example: Search 20 in BST:

      15
     /  \
    10   20


→ Found at right child of root.

3. Deletion in BST

Definition:
Deletion means removing a node from BST while maintaining the BST property.

Algorithm Steps (Simple):

Case 1: Node is Leaf
* Simply remove the node.

Case 2: Node has One Child
* Link parent to the child and remove node.

Case 3: Node has Two Children
* Find inorder predecessor (max of left subtree) or inorder successor (min of right subtree).
* Replace node value with predecessor/successor.
* Delete the predecessor/successor node.

Example: Delete 10 from BST:

      15
     /  \
    10   20
      \
      12

→ After deletion (replace 10 with 12):

      15
     /  \
    12   20


-----------


✅ GRAPH BASICS
1. Graph – Definition (2 lines)
A graph is a non-linear data structure consisting of a set of vertices (nodes) connected by edges.
It is used to represent networks, relationships, and connections.

2. Vertex (Node) – Definition (2 lines)
A vertex is a fundamental unit of a graph representing an entity or point.
Example: In a social network, a person can be a vertex.

3. Edge – Definition (2 lines)
An edge is a connection or link between two vertices in a graph.
It can be directed or undirected depending on the type of graph.

4. Degree of Vertex – Definition (2 lines)
Degree of a vertex is the number of edges incident to it.
Example: If a node has 3 connections → degree = 3.

5. Path – Definition (2 lines)
A path is a sequence of vertices where each pair of consecutive vertices is connected by an edge.
Example: A → B → C is a path.

6. Cycle – Definition (2 lines)
A cycle is a path that starts and ends at the same vertex without repeating any edge.
Example: A → B → C → A forms a cycle.

7. Likes / Connection – Definition (2 lines)
“Likes” in graph terms can be represented as edges showing a relation between two vertices.
Example: User A likes User B → edge from A to B.


----------


✅ TYPES OF GRAPHS
1. Directed Graph (Digraph)
A directed graph has edges with direction, i.e., edges go from one vertex to another in a specific direction.
Example: Social media “follow” relationship – A → B.

Diagram:
A → B → C
B → C

2. Undirected Graph
An undirected graph has edges without direction, i.e., connections are bidirectional.
Example: Friendship network – A and B are friends → edge A—B.

Diagram:
A — B
|   |
C — D

3. Weighted Graph
A weighted graph has edges assigned with a weight/cost (like distance, time, or cost).
Example: Road map – distance between cities as edge weights.

Diagram:
A —5— B
|     |
2     3
|     |
C —1— D

4. Unweighted Graph
An unweighted graph has edges without any weight, all connections are considered equal.
Example: Simple friendship network, no value assigned to connection.

Diagram:
A — B
|   |
C — D

5. Cyclic Graph
A cyclic graph contains at least one cycle, i.e., a path starting and ending at the same vertex.
Example: A → B → C → A

Diagram:
A → B → C
↑       |
|_______|

6. Acyclic Graph
An acyclic graph has no cycles, i.e., no path starts and ends at the same vertex.
Example: Tree structure or DAG.

Diagram:
A → B → C
|

→ D

7. Connected Graph
A graph is connected if there is a path between every pair of vertices.
Example: All cities connected by roads.

Diagram:
A — B — C
|       |
D — E — F

8. Disconnected Graph
A graph is disconnected if at least one pair of vertices has no path between them.
Example: Two separate networks.

Diagram:
A — B    C — D


-------------

Graph Representation: Adjacency Matrix vs Adjacency List

✅ GRAPH REPRESENTATION
1. Definition (Two lines)

Graph representation is a way to store graph vertices and edges in a data structure.
Two common methods are Adjacency Matrix and Adjacency List.

2. Comparison / Notes (4 points)

Adjacency Matrix:
👉 Uses a 2D array of size V×V (V = number of vertices).
👉 matrix[i][j] = 1 if there is an edge between vertex i and j; else 0.
👉 Easy and fast to check if edge exists (O(1) time).
👉 Uses more memory (O(V²)), inefficient for sparse graphs.

Adjacency List:

👉 Uses an array of lists, each vertex stores a list of adjacent vertices.
👉 Efficient in memory usage (O(V+E)), good for sparse graphs.
👉 Slower to check if an edge exists (O(degree of vertex)).
👉 Traversing all neighbors is fast and space-efficient.

3. Example / Diagram
Graph:

Vertices: A, B, C
Edges: A-B, B-C


-----------

👉 Adjacency Matrix:

|   | A | B | C |
| - | - | - | - |
| A | 0 | 1 | 0 |
| B | 1 | 0 | 1 |
| C | 0 | 1 | 0 |


Adjacency List:

A → B
B → A → C
C → B


-----------


✅ GRAPH TRAVERSAL: DFS & BFS
1. Definition (Two lines)

DFS (Depth First Search): Traversal technique that explores as far as possible along each branch before backtracking.

BFS (Breadth First Search): Traversal technique that explores all neighbors of a vertex before moving to the next level.

2. Algorithm / Steps (Simple)
a) DFS (Depth First Search)
1. Start from a chosen vertex.
2. Visit the vertex and mark as visited.
3. Recursively visit unvisited adjacent vertices.
4. Backtrack when no unvisited adjacent vertex is left.

Example (Graph):
A — B — C
|    
D

DFS Traversal (from A): A → B → C → D

b) BFS (Breadth First Search)
1. Start from a chosen vertex.
2. Visit the vertex and mark as visited.
3. Enqueue all unvisited adjacent vertices.
4. Dequeue vertex from queue and repeat until queue is empty.

Example (Graph):
A — B — C
|    
D

BFS Traversal (from A): A → B → D → C

3. Notes / Points
1. DFS uses stack (can be recursion).
2. BFS uses queue.
3. DFS is good for pathfinding, topological sorting, cycle detection.
4. BFS is good for shortest path in unweighted graph.


-----------------


✅ DIJKSTRA’S SHORTEST PATH ALGORITHM
1. Definition (Two lines)

Dijkstra’s algorithm finds the shortest path from a source vertex to all other 
vertices in a weighted graph with non-negative weights.
It is widely used in network routing, GPS navigation, and graph problems.

2. Algorithm (Step-wise, simple)

1. Assign distance = 0 for source vertex, and ∞ for all other vertices.
2. Mark all vertices as unvisited.
3. Select the unvisited vertex with minimum distance as current.
4. For each unvisited neighbor, calculate tentative distance = current distance + edge weight.
5. If tentative distance < existing distance, update distance.
6. Mark current vertex as visited.
7. Repeat steps 3–6 until all vertices are visited.

3. Example (Weighted Graph)

       (A)
      /   \
   4 /     \ 2
    /       \
  (B)-------(C)
       5

Source: A

Shortest distance from A:

A → A = 0
A → B = 4
A → C = 2

Path: A → C → B (distance = 2 + 5 = 7)

4. Notes / Points
1. Works only with non-negative edge weights.
2. Uses greedy approach (always pick minimum distance vertex).
3. Can be implemented using arrays (O(V²)) or priority queue / min-heap (O(E log V)).
4. Finds shortest path from source to all vertices, not just one.


✅ MINIMUM SPANNING TREE (MST) ALGORITHMS

1. Definition (Two lines)
Prim’s Algorithm: Builds a Minimum Spanning Tree (MST) by starting from a single vertex and 
adding edges with minimum weight connecting the MST to remaining vertices.

Kruskal’s Algorithm: Builds an MST by sorting all edges by weight and 
adding them one by one, avoiding cycles.

2. Prim’s Algorithm (Step-wise, simple)
1. Start from any vertex, mark it as included in MST.
2. Find the minimum weight edge connecting MST to a vertex not in MST.
3. Add that vertex and edge to MST.
4. Repeat step 2–3 until all vertices are included.

Example:
Vertices: A, B, C
Edges: A-B(4), B-C(2), A-C(3)
MST (Prim): A → C → B, total weight = 3 + 2 = 5

3. Kruskal’s Algorithm (Step-wise, simple)
1. Sort all edges by increasing weight.
2. Pick the smallest edge.
3. Add edge to MST if it does not form a cycle.
4. Repeat steps 2–3 until all vertices are connected.

Example:
Edges sorted: B-C(2), A-C(3), A-B(4)
Add B-C → A-C → MST complete
Total weight = 2 + 3 = 5

4. Notes / Points
1. Both algorithms produce Minimum Spanning Tree (MST).
2. Prim’s works vertex by vertex, Kruskal’s works edge by edge.
3. Prim’s uses adjacency matrix/list, Kruskal’s uses disjoint-set (union-find).
4. Prim’s better for dense graphs, Kruskal’s better for sparse graphs.