Exponent m^n

<!-- prettier-ignore -->
> (2^5 = 2 * 2 * 2 * 2 * 2 )

<!-- prettier-ignore -->
> m^n = m * m * m * m * m * m... for n times

<!-- prettier-ignore -->
> pow(m, n) = m * m * ... * m

```c
int pow(int m, int n)
{
  if (n == 0)
    return 1;
  else
    return pow(m, n - 1) * m;
}

```

optimal version

```c
int pow(int m, int n)
{
  if (n == 0)
    return 1;
  if (n % 2 == 0)
    return pow(m * m, n / 2);
  else
    return m * pow(m * m, (n - 1) / 2);
}
```
