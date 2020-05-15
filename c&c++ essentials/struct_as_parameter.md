```c
struct Rectangle
{
  int length;
  int breadth;
};

int area(struct Rectangle r1) // call by value
{
  return r1.length * r1.breadth;
}

int main()
{
  struct Rectangle r = {10, 5};
  printf("%d", area(r));
}
```

```c
struct Rectangle
{
  int length;
  int breadth;
};

int area(struct Rectangle& r1) // call by reference
{
  return r1.length * r1.breadth;
}

int main()
{
  struct Rectangle r = {10, 5};
  printf("%d", area(r));
}
```

```c
struct Rectangle
{
  int length;
  int breadth;
};

void changeLength(struct Rectangle* p, int l) // call by address
{
  p->length = l;
}

int main()
{
  struct Rectangle r = {10, 5};
  changeLength(&r, 20);
}
```

```c
struct Test
{
  int A[5];
  int n;
};

void fun(struct Test t1) // can only pass by value
{
  t1.A[0] = 10;
  t1.A[1] = 9;
}

int main()
{
  struct Test t = {{2, 4, 6, 8, 10}, 5};
  fun(t);
}
```
