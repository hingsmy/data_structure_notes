## Pointers

1. Why pointers
1. Declaration
1. Initialization
1. Dereferencing
1. Dynamic Allocation

---

- Accessing Heap
- Accessing Resource
- Parameter Passing

Data Variable

```c
int a = 10;
```

Address Variable

```c
int *p; // declaration
p = &a; // initialized with some value
printf('%d', d); // 10
printf('%d', *p); // dereferencing
```

### Acessing Heap

```c
#include <stdlib.h>
int main()
{
  int *p;
  p = (int *)malloc(5 * sizeof(int)); // 5 * 2
  // p = new int[5]; -- c++ style
}
```
