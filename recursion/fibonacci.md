```c
int fib(int b)
{
  if (n <= 1)
    return n;
  return fib(n - 2) + fib(n - 1);
}
```

```c
int fib(int n)
{
  int t0 = 0, t1 = 1, s, i; // -- 1
  if (n <= 1)
    return n; // -- 1
  for (i = 2; i <= n; i++) // -- n
  {
    s = t0 + t1; // -- n - 1
    to = t1; // -- n - 1
    t1 = s; // -- n - 1
  }
  return s; // -- 1
}
// 4n O(n)
```

Memoization

```c
int F[10];
int fib(int n)
{
  if (n <= 1)
  {
    F[n] = n;
    return n;
  }
  else
  {
    if (F[n-2] == -1)
      F[n-2] = fib(n-2);
    if (F[n-1] == -1)
      F[n-1] = fib(n-1);
    F[n] = F[n-2] + F[n-1];
    return F[n-2] + F[n-1];
  }
}

```

details on page 10
