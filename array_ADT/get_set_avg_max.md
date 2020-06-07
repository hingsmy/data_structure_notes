|     | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A   | 8   | 3   | 9   | 15  | 6   | 10  | 7   | 2   | 12  | 4   |

Get

```
Get(index)
{
  if (index >= 0 && index < length)
    return A[index]
}
```

Set

```
Set(index, x)
{
  if (index >= 0 && index < length)
    A[index] = x;
}
```

Max

```
Max()
{
  max = A[0]; // --- 1
  for (i = 1; i < length; i++) // --- n
  {
    if (A[i] > max) // --- n - 1
    {
      max = A[i];
    }
  }
  return max;
}

// --- 2n + 1
// O(n)
```

Min

```
Min()
{
  min = A[0];
  for (i = 1; i < length; i++)
  {
    if (A[i] < min)
      min = A[i];
  }
  return min;
```

Sum

```
Sum()
{
  total = 0; // --- 1
  for (i = 0; i < length; i++) // --- n + 1
  {
    total = total + A[i]; // --- n
  }
  return total; // --- 1
}

// 2n + 3
// O(n)

Sum(A, n)
{
  if (n < 0)
    return 0;
  return Sum(A, n - 1) + A[n];
}
Call Sum(A, length - 1);
```

Avg

```
Avg()
{
  total = 0;
  for (i = 0; i < length; i++)
  {
    total = total + A[i];
  }
  return total / n;
}
```
