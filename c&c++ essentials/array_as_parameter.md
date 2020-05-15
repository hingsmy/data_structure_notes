```c
void fun(int A[], int n) // Array can not be passed by value. It is passed by address.
// can also write fun(int *A, int n) -> it can point to any element.
{
  int i;
  for (i = 0; i < n; i++)
    printf("%d", A[i]);
}
int main()
{
  int A[5] = {2, 4, 6, 8, 10};
  fun(A, 5);
}
```

```c
void fun(int A[], int n)
{
  A[0] = 25; // change actual parameter.
}
int main()
{
  int A[5] = {2, 4, 6, 8, 10};
  fun(A, 5);
}
```

returning by array

```c
int[] fun(int n)
{
  int *p;
  p = (int*)malloc(n * sizeof(int));
  return p;
}
int main()
{
  int *A;
  A = fun(5);
}
```

```c
int* fun(int n)
{
  int *p;
  p = (int*)malloc(n * sizeof(int));
  return p;
}
int main()
{
  int *A;
  A = fun(5);
}
```
