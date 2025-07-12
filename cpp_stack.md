# Stack in C++

## 1. Overview

A **stack** is a linear data structure that follows the **LIFO (Last-In, First-Out)** principle.\
It allows adding (push) and removing (pop) elements only at one end, called the **top**.

---

## 2. Visual Representation

```
|   30   |  <-- top
|   20   |
|   10   |
-----------
```

- **Push:** Add element at the top.
- **Pop:** Remove element from the top.
- **Top/Peek:** View top element.
- **IsEmpty:** Check if stack is empty.
- **Size:** Get number of elements.

---

## 3. Stack in C++ STL

### Header

```cpp
#include <stack>
```

### Template Syntax

```cpp
std::stack<Type, Container>
```

- `Type` is the data type (e.g., `int`, `string`).
- `Container` is the underlying storage (default: `std::deque`).

### Main Operations

| Operation | Description             |
| --------- | ----------------------- |
| `push(x)` | Add x to the top        |
| `pop()`   | Remove the top element  |
| `top()`   | Access the top element  |
| `empty()` | Check if stack is empty |
| `size()`  | Number of elements      |

### Example: Using std::stack

```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> s;

    s.push(10);
    s.push(20);
    s.push(30);

    cout << "Top: " << s.top() << endl; // 30

    s.pop();

    cout << "Top after pop: " << s.top() << endl; // 20
    cout << "Size: " << s.size() << endl; // 2

    while (!s.empty()) {
        cout << s.top() << " ";
        s.pop();
    }
    // Output: 20 10

    return 0;
}
```
