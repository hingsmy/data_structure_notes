### Indirect Recursion

```c
void funA(int n)
{
  if (n > 0)
  {
    printf("%d", n);
    funB(n - 1);
  }
  void funB(int n)
  {
    if (n > 1)
    {
      printf("%d", n);
      funA(n / 2);
    }
  }
}
```

skeleton:

```c
void A(int n)
{
  if (<--->)
  {
    ...
    B(n - 1);
  }
}
void B(int n)
{
  if (<--->)
  {
    ...
    A(n - 3);
  }
}
```
