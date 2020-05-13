1. ### What are Functions
1. ### Paramater Passing

- Pass by Value
- Pass by Address
- Pass by Reference

---

- Monolithic Programming
- Modular Programming / Procedural Programming
- Object Oriented Programming

---

```c
// prototype / header / signiture // declaration
int add(int a, int b) // formal parameter
{ // definition
  int c;
  c = a + b;
  return c;
}
int main()
{
  int x, y, z;
  x = 10;
  y = 5;
  z = add(x, y); // actual parameter
  printf('sum is %d', z);
}
```
