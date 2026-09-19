# Check if an Array is Sorted

A simple Python program that checks whether the elements of an array are arranged in non-decreasing order.

## Overview

The program examines each element alongside the value immediately before it. If a smaller value appears after a larger one, the array is considered unsorted and the function immediately returns `False`.

If no such pair is found during the traversal, the function returns `True`.

## How It Works

The `isSorted()` function receives the array and its size:

```python
def isSorted(arr, n):
```

The loop begins from index `1` because every element needs to be compared with its predecessor:

```python
for i in range(1, n):
```

For each position, the program checks:

```python
if arr[i] < arr[i - 1]:
    return False
```

A violation means the array is not sorted, so there is no need to examine the remaining elements.

If the entire array passes the comparisons, the function returns:

```python
return True
```

This behavior is implemented directly in the uploaded program.

## Example

The program tests:

```python
arr = [1, 2, 3, 4, 5]
```

Since every element is greater than or equal to the element before it, the result is:

```text
True
```

The array and its length are passed to `isSorted()` before printing the result.

## Algorithm

1. Start from the second element.
2. Compare it with the previous element.
3. If the current element is smaller, return `False`.
4. Continue until the end of the array.
5. If no violation is found, return `True`.

## Complexity

| Metric          | Complexity |
| --------------- | ---------- |
| Time            | O(N)       |
| Auxiliary Space | O(1)       |

The function uses a single traversal and does not create another array.

## Key Concept

This program demonstrates how an array's ordering can be verified without sorting it first. Instead of rearranging elements, it only checks the relationship between neighboring values.

## Running the Program

Save the file and run:

```bash
python "Check if an Array is Sorted.py"
```

For the provided input, the output is:

```text
True
```
