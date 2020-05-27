```c
int c(int n, int r)
{
  int t1, t2, t3;
  t1 = fact(n); // n
  t2 = fact(r); // n
  t3 = fact(n-r); // n

  return t1/(t2 * t3); // 1
}

//3n --- O(n);
```

```c
int c(int n, int r)
{
  if (r == 0 || n == r)
    return 1;
  else
    return c(n-1, r-1) + c(n-1, r);
}
```

details on page 11.
