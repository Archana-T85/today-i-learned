# Today I Learned (TIL)

## Topic

System.arraycopy()

### What is it?

System.arraycopy() is a static method of the System class that efficiently copies elements from one array to another.

### Syntax

java
System.arraycopy(sourceArray,
                 sourcePosition,
                 destinationArray,
                 destinationPosition,
                 numberOfElements);


### Parameters

sourceArray – The array from which elements are copied.
sourcePosition – Starting index in the source array.
destinationArray – The array where elements are copied.
destinationPosition – Starting index in the destination array.
numberOfElements – Total number of elements to copy.

### Why do we use it?

* To copy elements efficiently between arrays.
* It is faster than copying elements one by one using a loop.
* Useful when creating a larger array because Java arrays have a fixed size.

### Example

java
int[] arr = {10, 20, 30, 40, 50};
int[] newArr = new int[10];

System.arraycopy(arr, 0, newArr, 0, arr.length);


### What I understood

* Java arrays have a fixed size.
* We cannot increase an existing array's size.
* To store more elements, we must:

  1. Create a new larger array.
  2. Copy the existing elements.
  3. Use the new array.
* System.arraycopy() makes this copying efficient.

### Real-world Usage

Classes like ArrayList automatically create a larger internal array when they run out of capacity and copy the existing elements into the new array before adding more data.

### Key Takeaways

* Arrays are fixed in size.
* System.arraycopy() performs fast array copying.
* The original array remains unchanged after copying.
* Reassigning the reference (arr = newArr) makes the variable point to the larger array.
* This concept is fundamental to understanding how dynamic data structures such as ArrayList work internally.
