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
// time - O(n)
// space - O(n)
```

```c
int sum(int n)
{
  return n * (n+1) / 2;
}
// O(1)
```

```c
int sum(int n)
{
  int i,s = 0; // -- 1
  for (i = 1; i <= n; i++) // -- n + 1
  {
    s = s + i; // -- n
  }
  return s; // -- 1
}

// O(n)
```

details on page 6.
