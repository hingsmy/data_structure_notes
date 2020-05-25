1 + 2 + 3 + 4 + 5 + 6 + 7 = ?

1 + 2 + 3 + 4 + 5 + 6 + 7 + ... + n =

sum(n) = 1 + 2 + 3 + ... + (n-1) + n

sum(n) = sum(n-1) + n

```c
int sum(int n)
{
  if (n == 0)
    return 0;
  else
    return sum(n-1) + n;
}
```

details on page 6.
