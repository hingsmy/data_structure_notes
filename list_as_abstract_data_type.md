### List

- store a given number of elements of a given data-type
- write / modify element at a position
- read element at a position

> Example: Arrays
>
> - int A[10];
> - A[i] = 2;
> - print A[i];

### Dynamic list

- empty list has size 0
- insert
- remove
- count
- read / modify element at a position
- specify data-type

---

A: 2 4 5 6 7 9 ---> A: 4 5 6 7 9

---

> - int A[MAXSIZE];
> - int end = -1;

> - insert(2)
> - insert(4)
> - insert(6)
> - insert(7)
> - insert(9)
> - insert(5, 2)
> - remove(0)

When array is full, create a new larger array, copy previous array into the new array.
free the memory for the previous array.

1. Access - read / write element at an index --> constant time O(1)
1. Insert - T ∝ n --> O(n)
1. Remove - T ∝ n --> O(n)
1. Add - T ∝ n --> O(n)
