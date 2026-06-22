# Dynamic Memory Allocation for Structures in C

## Overview

This project demonstrates how to dynamically allocate memory for a structure using `malloc()` in C. The program creates a `Car` structure, allocates memory at runtime, stores data using a pointer, and releases the allocated memory using `free()`.

---

## Concepts Covered

- Structures (`struct`)
- Dynamic Memory Allocation
- `malloc()`
- Structure Pointers
- Arrow Operator (`->`)
- Memory Deallocation using `free()`
- String Handling with `strcpy()`

---

## Project Description

The program defines a structure named `Car` with:

- `brand` → Character array to store the car brand
- `year` → Integer to store the manufacturing year

```c
struct Car {
    char brand[50];
    int year;
};
```

Memory for the structure is allocated dynamically using:

```c
struct Car *ptr = (struct Car*) malloc(sizeof(struct Car));
```

After successful allocation:

- Brand is assigned using `strcpy()`
- Year is assigned using the structure pointer
- Values are printed using the arrow (`->`) operator
- Allocated memory is released using `free()`

---

## Memory Allocation

```c
struct Car *ptr = (struct Car*) malloc(sizeof(struct Car));
```

This allocates memory at runtime for:

```text
brand[50] → 50 bytes
year      → 4 bytes

Total ≈ 54 bytes (+ padding depending on compiler)
```

---

## Accessing Structure Members

Since `ptr` is a pointer to a structure:

```c
ptr->year = 2022;
```

is equivalent to:

```c
(*ptr).year = 2022;
```

Similarly,

```c
strcpy(ptr->brand, "Honda");
```

stores the string `"Honda"` in the structure.

---

## Sample Output

```text
Brand: Honda
Year: 2022
```

---

## Program Flow

```text
Create Structure
       ↓
Allocate Memory using malloc()
       ↓
Check for NULL
       ↓
Store Values
       ↓
Display Data
       ↓
Free Memory
```

---

## Learning Outcomes

- Understanding structures in C
- Allocating memory dynamically for structures
- Using structure pointers
- Working with the arrow (`->`) operator
- Managing memory using `malloc()` and `free()`

---

## Real-World Applications

- Employee Management Systems
- Student Record Systems
- Vehicle Management Systems
- Embedded Systems
- Database Applications
- Dynamic Data Structures

---

## Time Complexity

```text
O(1)
```

All operations are performed in constant time.

---

## Space Complexity

```text
O(1)
```

Only one structure is dynamically allocated.

---

## Key Takeaway

Dynamic memory allocation allows structures to be created at runtime, making programs more flexible and memory efficient. Structure pointers combined with `malloc()` are widely used in real-world C applications and embedded systems.

---

## Author

**Amrutha D N**
```**
