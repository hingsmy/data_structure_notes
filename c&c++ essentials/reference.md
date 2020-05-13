### Reference

```c++
int main()
{
  int a = 10;
  int &r = a;
  cout << a; // 10
  r++;
  cout << r; // 11
  cout << a; // 11
}
```

> c++ only
