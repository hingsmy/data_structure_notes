```c
void TOH(int n, int A, int B, int C)
{
  if (n > 0)
  {
    TOH(n-1, A, C, B);
    printf("from %d to %d", A, C);
    TOH(n-1, B, A, C);
  }
}

TOH(3, 1, 2, 3);
```
