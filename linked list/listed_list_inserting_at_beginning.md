### Linked list: Inserting a node at beginning

Version 1

```c
#include <stdlib.h>
#include <stdio.h>

struct Node
{
  int data;
  struct Node *next;
};

struct Node *head;

void Insert(int x)
{
  struct Node *temp = (struct Node *)malloc(sizeof(struct Node));
  temp->data = x;
  temp->next = head;
  head = temp;
};
void Print()
{
  struct Node *temp = head;
  printf("List is: ");
  while (temp != NULL)
  {
    printf(" %d", temp->data);
    temp = temp->next;
  }
  printf("\n");
};
int main()
{
  head = NULL; // empty list
  printf("How many numbers?\n");
  int n, i, x;
  scanf("%d", &n);
  for (i = 0; i < n; i++)
  {
    printf("Enter the number \n");
    scanf("%d", &x);
    Insert(x);
    Print();
  }
}

```

Version 2

```c
#include <stdlib.h>
#include <stdio.h>

struct Node
{
  int data;
  struct Node *next;
};

struct Node *Insert(struct Node *head, int x)
{
  struct Node *temp = (struct Node *)malloc(sizeof(struct Node));
  temp->data = x;
  temp->next = head;
  head = temp;
  return head;
};
void Print(struct Node *head)
{
  printf("List is: ");
  while (head != NULL)
  {
    printf(" %d", head->data);
    head = head->next;
  }
  printf("\n");
};

int main()
{
  struct Node *head = NULL; // empty list
  printf("How many numbers?\n");
  int n, i, x;
  scanf("%d", &n);
  for (i = 0; i < n; i++)
  {
    printf("Enter the number \n");
    scanf("%d", &x);
    head = Insert(head, x);
    Print(head);
  }
}
```

Version 3

```c
#include <stdlib.h>
#include <stdio.h>

struct Node
{
  int data;
  struct Node *next;
};

void Insert(struct Node **head, int x)
{
  struct Node *temp = (struct Node *)malloc(sizeof(struct Node));
  temp->data = x;
  temp->next = NULL;
  if (*head != NULL)
    temp->next = *head;
  *head = temp;
};
void Print(struct Node *head)
{
  printf("List is: ");
  while (head != NULL)
  {
    printf(" %d", head->data);
    head = head->next;
  }
  printf("\n");
};

int main()
{
  struct Node *head = NULL; // empty list
  printf("How many numbers?\n");
  int n, i, x;
  scanf("%d", &n);
  for (i = 0; i < n; i++)
  {
    printf("Enter the number \n");
    scanf("%d", &x);
    Insert(&head, x);
    Print(head);
  }
}
```
