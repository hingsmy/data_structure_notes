Call by Value

```c
void swap(int x, int y)
{
  int temp;
  temp = x;
  x = y;
  y = temp;
}

int main()
{
  int a, b;
  a = 10;
  b = 20;
  swap(a, b);
  printf("%d %d", a, b); // 10 20
}
```

Call by Address

```c
void swap(int* x, int* y)
{
  int temp;
  temp = *x;
  *x = *y;
  *y = temp;
}

int main()
{
  int a, b;
  a = 10;
  b = 20;
  swap(&a, &b);
  printf("%d %d", a, b); // 20 10
}
```

Call by Reference

```c
void swap(int& x, int& y)
{
  int temp;
  temp = x;
  x = y;
  y = temp;
}

int main()
{
  int a, b;
  a = 10;
  b = 20;
  swap(a, b);
  printf("%d %d", a, b); // 20 10
}
```
