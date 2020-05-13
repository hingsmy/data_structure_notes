```c
struct Rectangle
{
  int length; // 2 bytes
  int breadth; // 2 bytes
};

int main()
{
  struct Rectangle r = {10, 5};
  struct Rectangle *p = &r; // 2 bytes
  r.length = 15;

  (*p).length = 20;
  p->length = 20;
}
```

### Create an object dynamically in heap using pointer

```c
struct Rectangle
{
  int length;
  int breadth;
}
  int main()
  {
    struct Rectangle *p;
    p = (struct Rectangle *)malloc(sizeof(struct Rectangle));
    p->length = 10;
    p->breadth = 5;
  }
```
