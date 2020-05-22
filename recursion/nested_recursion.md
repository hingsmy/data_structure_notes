Nested Recursion

```c
int fun(int n)
{
  if (n > 100)
  {
    return n - 10;
  }
  else
    return fun(fun(n + 1));
}
fun(95);
```

> detail on page 5.
