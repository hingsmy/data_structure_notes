Taylor series

```c
int e(int x, int n)
{
  static int p = 1, f = 1;
  int r;

  if (n == 0)
    return 1;
  else
  {
    r = e(x, n-1);
    p = p * x;
    f = f * n;
    return r + p / f;
  }
}
```

details on page 8

### Horner's rule

```c
double e(int x, int n)
{
  double s = 1;
  int i;
  double num = 1;
  double den = 1;

  for (i = 1; i <= n; i++)
  {
    num *= x;
    den *= i;
    s += num/den;
  }
  return s;
}
```

```c
double e(int x, int n)
{
  static double s;
  if (n == 0)
    return s;
  s = 1 + x / n * s;
  return e(x, n-1);
}
```
