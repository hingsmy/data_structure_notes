linear Recursion

```c
fun(n)
{
  if (n > 0)
  {
    ...
    fun(n - 1);
    ...
  }
}
```

Tree Recursion

```c
fun(n)
{
  if (n > 0)
  {
    ...
    ...
    fun(n - 1);
    ...
    ...
    fun(n - 1);
  }
}
```

Example:

```c
void fun(int n)
{
  if (n > 0)
  {
    printf("%d ", n);
    fun(n - 1);
    fun(n - 1)；
  }
}
fun(3);
```

> detailed note on page 4.
