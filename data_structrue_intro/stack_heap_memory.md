1. About main memory
1. How a program use memory
1. Static allocation
   the size of memory is static. Memory size determined at compile time, before run time
1. Dynamic allocation

```c
void main()
{
  int a; // 2bytes
  float b; // 4bytes

}
```

```c
void fun2(int i)
{
  int a;
}
void fun1()
{
  int x;
  fun2(x);
}
void main()
{
  int a;
  float b;
  fun1();
}
```

```c
void main()
{
  int* p;
  p = new int[5]; // c++
  p = (int* )malloc(2*5); // c
  //
  delete[]p;
  p = NULL;
}
```
