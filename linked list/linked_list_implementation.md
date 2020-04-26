### Linked List - Implementation in c / c++

```cpp
  struct Node
  {
    int data;
    struct Node* link;
  }

  Node* A;
  A = NULL; // empty list

  Node* temp = new Node();
  temp -> data = 2;
  temp -> link = NULL;
  A = temp;

  temp = new Node();
  temp -> data = 4;
  temp -> link = NULL;

  // Traversal
  Node* temp1 = A;
  while (temp1 -> link != NULL) {
    temp1 = temp1 -> link;
  }

  temp1 -> link = temp;

```
