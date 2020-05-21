### Head Recursion

Function does not perform any kind of operations at the time of calling. All processing done at returning time.

```c
void fun(int n)
{
  if (n > 0)
  {
    fun(n-1);
    ...
    ...
  }
}
```

```c
void fun(int n)
{
  if (n > 0)
  {
    fun(n-1);
    printf("%d", n);
  }
}
fun(3);
```

convert to loop

```c
void fun(int n)
{
  int i = 1;
  while(i <= n)
  {
    printf("%d", n);
    i++;
  }
}
fun(3);
```
