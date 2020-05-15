```c++
#include <iostream>
using namespace std;
class Rectangle
{
private:
  int length;
  int breadth;
public:
  // Rectangle()
  // {
  //   length = 1;
  //   breadth = 1;
  // }
  Rectangle(int l, int b);

  int area(); // facilitator
  int perimeter(); // facilitator
  int getLength() { return length; } // accessor
  void setLength(int l) { length = l; } // mutator
  ~Rectangle(); // destructor
};

Rectangle::Rectangle(int l, int b)
{
  length = l;
  breadth = b;
}

int Rectangle::area()
{
  return length * breadth;
}
int Rectangle::perimeter()
{
  return 2 *  (length + breadth);
}
Rectangle::~Rectangle()
{}

int main()
{
  Rectangle r(10, 5);
  cout << r.area();
  cout << r.perimeter();
  r.setLength(20);
  cout << r.getLength();
}
```
