# **Pointers in C++**

## **AIM**

Understand and implement the concept of **Pointers** in C++.

## **Software Used**

* Visual Studio Code (VS Code)

---

## **Theory**

A **pointer** is a special type of variable that stores the **memory address** of another variable.
In C++, pointers are widely used for:

* Direct memory access
* Dynamic memory allocation
* Efficient handling of arrays and strings

---

## **1. Pointer Basics**

* Declared using an asterisk (`*`) before the variable name.

```cpp
int *ptr;
```

* Stores the address of another variable.

---

## **2. Pointer Arithmetic**

Pointers can be incremented (`ptr++`) or decremented to move to adjacent memory locations.

* For `int*` → moves by **4 bytes** (on most systems)
* For `double*` → moves by **8 bytes**
* For `char*` → moves by **1 byte**

This makes it possible to traverse arrays without using indexing.

---

## **3. Pointers and Arrays**

* The name of an array acts as a pointer to its first element.

```cpp
arr  ≡  &arr[0]
```

* Elements can be accessed as:

```cpp
*(arr + i)   // same as arr[i]
```

---

## **4. Strings and Pointers**

* C-style strings are stored as character arrays ending with `'\0'`.
* A `char*` pointer can be used to traverse each character until the null terminator.

---

## **5. Common Applications of Pointers**

* Traversing arrays without indexing
* Reversing arrays/strings using start and end pointers
* Calculating sums/differences using dereferencing
* Palindrome checking by comparing characters from both ends

---

## **6. Advantages of Pointers**

* Efficient data access and modification
* Enables **dynamic memory allocation**
* Passes large data structures to functions without copying

---

## **7. Precautions**

* Avoid **uninitialized pointers** (can cause undefined behavior)
* Prevent **out-of-bounds** memory access
* Always ensure a pointer points to valid memory before dereferencing

---

## **Algorithms**

### **1. Pointer Arithmetic on Different Data Types**

**Aim:** Demonstrate how pointer increments differ for various data types.
**Steps:**

```
1. Start
2. Declare int, double, and bool variables
3. Create pointers to each variable
4. Print initial addresses
5. Increment pointers by 1
6. Print new addresses
7. Stop
```

---

### **2. Sum of Array Elements Using Pointers**

**Aim:** Calculate sum of array elements using pointer arithmetic.
**Steps:**

```
1. Start
2. Declare and initialize an integer array
3. Point a pointer to the first element
4. Initialize sum = 0
5. Loop through array:
   sum += *(ptr + i)
6. Print total sum
7. Stop
```

---

### **3. Reverse an Array Using Pointers**

**Aim:** Reverse elements of an array using two pointers.
**Steps:**

```
1. Start
2. Declare and initialize array
3. Find array length
4. Set ptr = first element, ptr1 = last element
5. While ptr < ptr1:
   Swap *ptr and *ptr1
   Increment ptr, decrement ptr1
6. Print reversed array
7. Stop
```

---

### **4. Check Palindrome Using Pointers**

**Aim:** Check if a string is a palindrome using two pointers.
**Steps:**

```
1. Start
2. Read string
3. Set start = first char, end = last char before '\0'
4. While start < end:
   If *start != *end → Not a palindrome, Stop
   Else increment start, decrement end
5. If loop completes → Palindrome
6. Stop
```

---

## **Conclusion**

Pointers are one of the **most powerful features** of C++, enabling direct memory manipulation and efficient data handling.
While extremely useful, they require **careful handling** to prevent issues such as segmentation faults and memory leaks.
Mastering pointers opens the door to **advanced programming techniques** like dynamic memory management, complex data structures, and efficient algorithms.


