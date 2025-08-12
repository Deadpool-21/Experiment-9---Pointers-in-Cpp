POINTERS IN C++

AIM: Understanding Pointers in C++

SOFTWARE USED: VS Code

THEORY

A pointer is a special type of variable that stores the memory address of another variable.
 In C++, pointers are extensively used for direct memory manipulation, dynamic memory allocation, and efficient handling of arrays and strings.

1. Basics of Pointers

Declared using an asterisk * before the variable name.


Example:

 cpp
CopyEdit
int *ptr;


ptr stores the address of an integer variable.




2. Pointer Arithmetic

Pointers can be incremented (ptr++) or decremented (ptr--).


The step size depends on the data type:


int* → usually 4 bytes


double* → usually 8 bytes


char* → 1 byte


This property enables easy traversal of arrays without using indices.



3. Pointers and Arrays

The array name acts as a pointer to its first element (arr is the same as &arr[0]).


Elements can be accessed as:


arr[i]


*(arr + i)



4. Strings and Pointers

A C-style string is a character array ending with the null terminator '\0'.


char* can be used to traverse characters until the null terminator is found.



5. Common Applications of Pointers

Traversing arrays without indexing


Reversing arrays or strings using start and end pointers


Calculating sums/differences by dereferencing pointers


Checking palindromes by comparing characters from both ends



6. Advantages

Faster and more efficient data access


Supports dynamic memory allocation


Enables passing large structures or arrays to functions without copying data



7. Precautions 

Avoid uninitialized pointers (undefined behavior)


Accessing memory outside the valid range can cause program crashes


Always ensure a pointer points to valid memory before dereferencing



ALGORITHMS
1. Pointer Arithmetic on Different Data Types

Aim: Show how pointer increments vary with data type sizes.
 Steps:
Start


Declare variables of type int, double, and bool


Create pointers for each variable and print their initial addresses


Increment each pointer by 1


Print new addresses to observe differences


Stop



2. Sum of Array Elements Using Pointers

Aim: Compute sum of array elements via pointer arithmetic.
 Steps:
Start


Declare and initialize an integer array


Point a pointer to the first array element


Set sum = 0


Loop through array elements: sum += *(ptr + i)


Print total sum


Stop



3. Reverse an Array Using Pointers

Aim: Reverse array elements with two pointers.
 Steps:
Start


Declare and initialize an array


Find array length


Set ptr to the first element, ptr1 to the last element


While ptr < ptr1: swap values, increment ptr, decrement ptr1


Print reversed array


Stop



4. Palindrome Check Using Pointers
If *start != *end → print "Not a palindrome" and stop
Aim: Determine if a string is a palindrome.
 Steps:
Start


Read string input


Set start to first character, end to last character before '\0'


While start < end:




Else increment start, decrement end


If loop completes → print "Palindrome"


Stop



Conclusion
Pointers are a core feature of C++, allowing direct access to memory and flexible data manipulation. They enable powerful operations like dynamic memory management and efficient handling of large datasets. However, incorrect pointer usage can lead to crashes, undefined behavior, or memory leaks, so they must be handled with care.
