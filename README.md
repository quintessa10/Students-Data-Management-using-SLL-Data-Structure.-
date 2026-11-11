# Student Data Management System

The Student Data Management System is a console-based application written in C that utilizes a Singly Linked List (SLL) data structure to efficiently manage and manipulate student records.[cite: 1] This project demonstrates core concepts of Data Structures and Algorithms (DSA), dynamic memory allocation, and file handling in C without relying on fixed-size arrays.[cite: 1] Each student record is stored as a node in the linked list containing three primary data fields: Roll Number (integer), Name (string), and Marks (float), along with a pointer to the next record.[cite: 1]

## Key Features & Functionalities

* **1. Add New Record:** Dynamically allocates memory for a new student and appends their roll number, name, and marks to the end of the linked list.[cite: 1]
* **2. Delete a Record:** Searches for a specific student by their roll number, removes their node from the list, and safely frees the allocated memory to prevent memory leaks.[cite: 1]
* **3. Show the List:** Traverses the entire linked list from the head node to the end, displaying all stored student records in a clean format.[cite: 1]
* **4. Modify a Record:** Allows the user to search for a student by their roll number and update their name.[cite: 1]
* **5. Save Record:** Implements file handling to export the current linked list data into a text file (std.txt), ensuring data persists even after the program is closed.[cite: 1]
* **6. Sort the List:** Reorders the student records alphabetically by name using a sorting algorithm that swaps the data within the nodes.[cite: 1]
* **7. Delete All Records:** Iterates through the list and deletes every node one by one (with a visual 1-second delay between deletions), completely clearing the list and freeing all heap memory.[cite: 1]
* **8. Reverse the List:** Traverses and prints the student records in reverse order (from the last added to the first).[cite: 1]
* **9. Safe Exit:** Automatically frees all dynamically allocated memory before terminating the program to ensure efficient resource management.[cite: 1]

## Technical Concepts Applied

* **A. Singly Linked Lists (SLL):** Core data structure for storing records sequentially via pointers.[cite: 1]
* **B. Dynamic Memory Allocation:** Use of `malloc()` and `free()` for real-time memory management.[cite: 1]
* **C. File Handling:** Using `fopen()`, `fprintf()`, and `fclose()` for persistent data storage.[cite: 1]
* **D. Pointer Manipulation:** Extensive use of single (`SLL *`) and double pointers (`SLL **`) to modify the head pointer directly from sub-functions.[cite: 1]
* **E. String Operations:** Using `<string.h>` library functions like `strcmp()` and `strcpy()` for data comparison and modification.[cite: 1]
