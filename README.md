# PLS_assignment


## Memory Allocation in Arrays: C++ vs Python

This section explains different types of array memory allocation (fixed/stack/heap dynamic) in **C++** and **Python** with code examples.

---

## 🔹 Fixed Stack Dynamic

**C++:**
```cpp
int myArr[5];
```
- Array size is fixed at compile time (`5`).
- Memory is allocated on the stack.

**Python:**
```python
myArray = [0] * 5
```
- Python does not support fixed-size arrays by default.
- This is a simulation of fixed-size behavior.
- Size is fixed (`5`), but the list is still dynamic internally and allocated on the heap.

---

## 🔹 Stack Dynamic

**C++:**
```cpp
void myFunc(int size) {
    int myArr[size];
}
```
- Array size is determined at **run time**.
- Memory is allocated on the **stack**.

**Python:**
```python
def myFunc(size):
    myArr = [0] * size
```
- Similar behavior: size is defined during runtime.
- Memory is allocated on the **heap**, as Python does not use stack allocation for such objects.

---

## 🔹 Fixed Heap Dynamic

**C++:**
```cpp
int* arr = new int[5];
// use arr...
delete[] arr;
```
- Array of size `5` is allocated on the **heap**.
- Must manually free memory using `delete[]`.

**Python:**
```python
myArr = [i * 2 for i in range(10)]
```
- Array size is fixed (`10`).
- Memory is automatically managed and allocated on the **heap**.

---

## 🔹 Heap Dynamic

**C++:**
```cpp
#include <vector>
#include <iostream>
using namespace std;

vector<int> myArr;
myArr.push_back(5);
myArr.push_back(10);
myArr.push_back(15);
```
- `vector` grows and shrinks dynamically at runtime.
- Memory is allocated on the **heap**.

**Python:**
```python
myArr = []
myArr.append(5)
myArr.append(8)
print(myArr)
```
- Python lists are dynamic and grow/shrink as needed.
- All lists are allocated on the **heap**.
