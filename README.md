# Algorithm Battle – Which Data Structure Wins?

## Project
Student Record Management System comparing Binary Search Tree (BST),
AVL Tree, and Hash Table using Linear Probing.

## Repository structure

```text
Algorithm-Battle/
├── student.c
├── README.md
├── Report.docx                 # Add your final report here
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

## Compile and run

```bash
gcc -std=c99 -Wall -Wextra student.c -o student
./student
```

## Dataset
The program starts with 30 records (IDs 1001–1030). The screenshots also
document insertion of an additional test record: ID 1031, name `student`,
department `CSE`, marks `75`.

## Test evidence
Screenshots document successful and unsuccessful searches in all three
structures, BST and AVL traversals, dataset display, insertion, and the
performance experiment.

## Performance output captured
The submitted terminal screenshot records:
- Dataset size: 30
- BST height: 30; successful comparisons: 15; unsuccessful comparisons: 30
- AVL height: 5; successful comparisons: 5; unsuccessful comparisons: 5
- Hash table size: 47; insertion collisions: 300
- Hash successful search probes for ID 1015: 10
- Hash unsuccessful search probes for ID 1099: 22

Use the final program output as the source of truth when updating the report.

## GitHub repository URL
Add your actual repository URL after creating the repository:
`https://github.com/YOUR-USERNAME/Algorithm-Battle`

## Final report
Add your completed report to this folder as `Report.docx`.
