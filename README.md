# Algorithm Battle – Which Data Structure Wins?

## Project overview

This project implements a **Student Record Management System in C** and compares the performance of three data structures:

- **Binary Search Tree (BST)** – stores student records according to Student ID.
- **AVL Tree** – a self-balancing binary search tree.
- **Hash Table with Linear Probing** – stores records using a hash function and resolves collisions by checking the next available slot.

Each student record contains a Student ID, name, department, and marks.

## Dataset

The program initially loads **30 student records**, with Student IDs from **1001 to 1030**. The records are inserted into the BST, AVL Tree, and hash table in ascending Student ID order.

The initial dataset uses the following record pattern:

- Student IDs: `1001`–`1030`
- Names: `Student 1`–`Student 30`
- Departments: `CSE`, `ECE`, `IT`, and `EEE`
- Marks: individual marks are assigned to each record in `student.c`

## Data structure configuration

| Parameter | Value |
|---|---|
| Initial number of records | 30 |
| Student ID range | 1001–1030 |
| Maximum student capacity | 100 |
| Hash table size | 47 slots |
| Hash function | `h(id) = id % 10` |
| Collision handling | Linear Probing |
| Successful search key | 1015 |
| Unsuccessful search key | 1099 |

## Features and menu options

The program provides the following menu-driven operations:

| Option | Operation |
|---:|---|
| 1 | Search using BST |
| 2 | Search using AVL Tree |
| 3 | Search using Hashing |
| 4 | Display BST traversals |
| 5 | Display AVL Tree traversals |
| 6 | Display Hash Table |
| 7 | Insert a new student record |
| 8 | Run the performance experiment |
| 9 | Display all student records |
| 0 | Exit |

The BST and AVL Tree support inorder, preorder, and postorder traversals. The program also measures search comparisons, hash probes, tree heights, and insertion collisions.

## Compile and run

A C compiler such as GCC is required.

**Linux / macOS:**

```bash
gcc -std=c99 -Wall -Wextra student.c -o student
./student
```

**Windows (GCC / MinGW):**

```bash
gcc -std=c99 -Wall -Wextra student.c -o student.exe
student.exe
```

## Performance experiment

The following results are produced by running menu option **8** with the initial 30-record dataset:

| Measurement | BST | AVL Tree | Hash Table |
|---|---:|---:|---:|
| Tree height (nodes) | 30 | 5 | Not applicable |
| Successful search (ID 1015) | 15 comparisons | 5 comparisons | 10 probes |
| Unsuccessful search (ID 1099) | 30 comparisons | 5 comparisons | 22 probes |
| Insertion collisions | Not applicable | Not applicable | 300 |

The results depend on the insertion order and hash function used in this experiment. Since the records are inserted in ascending order, the ordinary BST becomes right-skewed. The AVL Tree remains balanced through rotations. Linear probing encounters clustering with the selected hash function.

## Repository structure

```text
algorithm-Battle/
├── student.c
├── README.md
├── report.docx
└── Screenshots/
    ├── initial_dataset_30_students.png
    ├── insert_student_1031.png
    ├── dataset_after_insertion_1031.png
    ├── bst_successful_search_1015.png
    ├── avl_successful_search_1015.png
    ├── hash_successful_search_1015.png
    ├── bst_unsuccessful_search_1099.png
    ├── avl_unsuccessful_search_1099.png
    ├── hash_unsuccessful_search_1099.png
    ├── bst_inorder_traversal.png
    ├── bst_preorder_traversal.png
    ├── bst_postorder_traversal.png
    ├── avl_inorder_traversal.png
    ├── avl_preorder_traversal.png
    ├── avl_postorder_traversal.png
    └── performance_comparison.png
```

Add genuine screenshots captured from running the program to the `Screenshots` folder. The insertion screenshots should show the values actually entered during the insertion test.

## GitHub repository

https://github.com/Navin-13/algorithm-Battle

## Report

Keep the completed project report in the repository root as `report.docx`.
