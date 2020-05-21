Tail Recursion

```c
void fun(int n)
{
  if (n > 0)
  {
    printf("%d", n);
    fun(n-1);
  }
}
fun(3);
```

> Space complexity - O(n)

### convert to loop

```c
void fun(int n)
{
  while (n > 0)
  {
    printf("%d", n);
    n--;
  }
}
fun(3)
```

> Space complexity - O(1)

Time complexity are both O(n)
