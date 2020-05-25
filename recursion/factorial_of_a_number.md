n! = 1 _ 2 _ 3 _ 4 _ ... \* n

5! = 1 _ 2 _ 3 _ 4 _ 5 = 120

fact(n) = 1 _ 2 _ 3 _ ... _ (n-1) \* n

fact(n) = fact(n-1) \* n

```c
int fact(int n)
{
  if (n == 0)
    return 1;
  else
    return fact(n-1) * n;
}
```
