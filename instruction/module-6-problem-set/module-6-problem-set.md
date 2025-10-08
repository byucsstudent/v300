# Module 6 Problem Set

This problem set is designed to reinforce the concepts covered in Module 6. Working through these problems will help you solidify your understanding of the material and prepare you for upcoming assessments. Remember to focus on understanding the *why* behind each solution, not just memorizing the steps. Good luck!

## Problem 1: Data Structures and Algorithms

This problem explores the relationship between data structures and algorithms. You will be assessed on your ability to select the appropriate data structure for a given algorithmic task.

**Problem:**

You are tasked with creating a program that efficiently stores and retrieves user information. Each user has a unique ID (an integer) and a name (a string). The program must support the following operations:

1.  **Insert:** Add a new user with their ID and name.
2.  **Search:** Given a user ID, quickly retrieve the corresponding name.
3.  **Delete:** Given a user ID, remove the user from the data store.
4.  **List (optional):** Display all users in sorted order by ID. This is less critical for immediate performance but should be considered.

**Questions:**

*   Which data structure would be most suitable for this task? Justify your choice, considering the time complexity of each operation.
*   Describe the algorithm you would use for each of the required operations (Insert, Search, Delete).
*   What are the trade-offs involved in using your chosen data structure compared to alternative options like a simple array or linked list?
*   How would your choice change if the number of users was extremely large (e.g., millions)?

**Example:**

Let's say you choose a hash table.

*   **Data Structure:** Hash Table
*   **Justification:** Hash tables offer average-case O(1) time complexity for insert, search, and delete operations, making them very efficient for large datasets.
*   **Algorithms:**
    *   **Insert:** Calculate the hash value of the user ID and store the user data at the corresponding index in the hash table. Handle collisions using a technique like chaining or open addressing.
    *   **Search:** Calculate the hash value of the user ID and retrieve the user data from the corresponding index. Handle collisions by traversing the chain or probing for the correct entry.
    *   **Delete:** Calculate the hash value of the user ID and remove the user data from the corresponding index. Handle collisions appropriately based on the collision resolution strategy.
*   **Trade-offs:** Compared to an array, a hash table offers much faster search and delete operations (O(1) vs. O(n) in the worst case). Compared to a linked list, it offers faster search (O(1) vs. O(n)). However, hash tables require more memory and can have worst-case O(n) performance if there are many collisions. The optional List operation is not naturally supported in sorted order.

**Common Challenges and Solutions:**

*   **Challenge:** Choosing between a hash table and a balanced tree (e.g., AVL tree, Red-Black tree). Balanced trees offer guaranteed O(log n) performance for all operations, including sorted iteration.
    *   **Solution:** Consider the frequency of each operation. If search, insert, and delete are performed much more often than listing, a hash table might be preferable. If sorted iteration is critical, a balanced tree might be a better choice.
*   **Challenge:** Handling hash collisions effectively.
    *   **Solution:** Implement a robust collision resolution strategy (e.g., separate chaining with linked lists or open addressing with double hashing).  Consider the load factor of the hash table and resize it dynamically to maintain good performance.

## Problem 2: Algorithm Analysis and Big O Notation

This problem tests your ability to analyze the time complexity of algorithms using Big O notation.

**Problem:**

Analyze the time complexity of the following code snippets:

**Snippet 1 (Python):**

```python
def find_max(arr):
  max_val = arr[0]
  for i in range(1, len(arr)):
    if arr[i] > max_val:
      max_val = arr[i]
  return max_val
```

**Snippet 2 (Java):**

```java
public int binarySearch(int[] arr, int target) {
    int low = 0;
    int high = arr.length - 1;

    while (low <= high) {
        int mid = low + (high - low) / 2;

        if (arr[mid] == target) {
            return mid;
        } else if (arr[mid] < target) {
            low = mid + 1;
        } else {
            high = mid - 1;
        }
    }

    return -1; // Target not found
}
```

**Snippet 3 (C++):**

```cpp
#include <iostream>
#include <vector>

void printPairs(const std::vector<int>& arr) {
    for (size_t i = 0; i < arr.size(); ++i) {
        for (size_t j = 0; j < arr.size(); ++j) {
            std::cout << arr[i] << ", " << arr[j] << std::endl;
        }
    }
}
```

**Questions:**

*   Determine the Big O notation for each code snippet. Explain your reasoning.
*   For Snippet 2 (binary search), what assumptions are you making about the input array?
*   How would the time complexity of Snippet 3 change if the inner loop iterated from `j = i` instead of `j = 0`?

**Example:**

For Snippet 1 (finding the maximum value):

*   **Time Complexity:** O(n)
*   **Reasoning:** The code iterates through the array once, performing a constant amount of work (comparison) for each element. Therefore, the time complexity grows linearly with the size of the input array (n).

**Common Challenges and Solutions:**

*   **Challenge:** Confusing constant factors with Big O notation.
    *   **Solution:** Big O notation describes the *growth rate* of an algorithm's runtime. Constant factors (e.g., 2n vs. n) are ignored because they become insignificant as n becomes very large.
*   **Challenge:** Accurately identifying nested loops.
    *   **Solution:** The time complexity of nested loops is often the product of the number of iterations of each loop.  Be careful about the loop bounds.

## Problem 3: Recursion and Dynamic Programming

This problem explores the concepts of recursion and dynamic programming.

**Problem:**

Implement a function to calculate the nth Fibonacci number using both recursion and dynamic programming.

**Questions:**

*   Write a recursive function to calculate the nth Fibonacci number. Analyze its time complexity.
*   Write a dynamic programming function (using memoization or tabulation) to calculate the nth Fibonacci number. Analyze its time complexity.
*   Compare and contrast the two approaches. What are the advantages and disadvantages of each?
*   For what values of n does the recursive approach become impractical?

**Example (Recursive Approach - Python):**

```python
def fibonacci_recursive(n):
  if n <= 1:
    return n
  else:
    return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)
```

**Example (Dynamic Programming - Memoization - Python):**

```python
def fibonacci_memoization(n, memo={}):
  if n in memo:
    return memo[n]
  if n <= 1:
    return n
  else:
    result = fibonacci_memoization(n-1, memo) + fibonacci_memoization(n-2, memo)
    memo[n] = result
    return result
```

**Common Challenges and Solutions:**

*   **Challenge:** Understanding the exponential time complexity of the naive recursive Fibonacci implementation.
    *   **Solution:** Draw the recursion tree to visualize the repeated calculations of the same Fibonacci numbers.
*   **Challenge:** Implementing memoization correctly.
    *   **Solution:** Ensure that you are storing the results of intermediate calculations in the memo and checking the memo before making recursive calls.
*   **Challenge:** Choosing between memoization and tabulation.
    *   **Solution:** Memoization is a top-down approach, starting with the desired result and recursively breaking it down. Tabulation is a bottom-up approach, building up the solution from the base cases. Memoization can be more intuitive, while tabulation can be slightly more efficient in some cases by avoiding recursion overhead.

## External Resources

*   **Big O Cheat Sheet:** [https://www.bigocheatsheet.com/](https://www.bigocheatsheet.com/) - A quick reference for common data structure and algorithm time complexities.
*   **Khan Academy Algorithms Course:** [https://www.khanacademy.org/computing/computer-science/algorithms](https://www.khanacademy.org/computing/computer-science/algorithms) - A comprehensive introduction to algorithms and data structures.

## Summary

This problem set covered key concepts from Module 6, including data structures, algorithm analysis (Big O notation), recursion, and dynamic programming. By working through these problems, you have gained valuable experience in applying these concepts to solve practical problems. Remember to review the solutions and explanations carefully to solidify your understanding. Continue practicing and exploring these topics to further develop your skills.
