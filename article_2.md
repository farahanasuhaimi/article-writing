Sure, let me explain the concept of time and space complexity, represented by the Big O notation (O()).

Time Complexity:
Time complexity is a measure of how the running time of an algorithm scales with the input size. It quantifies the amount of time an algorithm takes to run as a function of the input size. The Big O notation is used to express the upper bound of the growth rate of an algorithm's running time.

Here are some common time complexities:

- O(1) - Constant Time: The algorithm's running time is constant, regardless of the input size. Example: Accessing an element in an array by its index.

- O(n) - Linear Time: The running time grows linearly with the input size. Example: Iterating over an array or a linked list.

- O(n^2) - Quadratic Time: The running time grows quadratically with the input size. Example: Nested loops over an array or a matrix.

- O(log n) - Logarithmic Time: The running time grows logarithmically with the input size. Example: Binary search on a sorted array.

- O(n log n) - Linearithmic Time: The running time grows as the product of linear and logarithmic factors. Example: Efficient sorting algorithms like Merge Sort and Quicksort.

The smaller the time complexity, the better the algorithm's performance, especially for large input sizes.

Space Complexity:
Space complexity is a measure of how much additional memory an algorithm requires as a function of the input size. It quantifies the amount of memory or space an algorithm takes to run.

Here are some common space complexities:

- O(1) - Constant Space: The algorithm's memory usage is constant, regardless of the input size.

- O(n) - Linear Space: The memory usage grows linearly with the input size.

- O(n^2) - Quadratic Space: The memory usage grows quadratically with the input size.

- O(log n) - Logarithmic Space: The memory usage grows logarithmically with the input size.

In general, algorithms with lower space complexity are preferred, as they use less additional memory, which can be crucial for large input sizes or memory-constrained environments.

In the case of the alternative solution for finding the second smallest number:

```python
def find_second_smallest(nums):
    smallest = float('inf')
    second_smallest = float('inf')

    for num in nums:
        if num < smallest:
            second_smallest = smallest
            smallest = num
        elif num < second_smallest and num != smallest:
            second_smallest = num

    return second_smallest if second_smallest != float('inf') else None
```

The time complexity of this solution is O(n), where n is the length of the input list `nums`. This is because the algorithm iterates through the list once, performing constant-time operations for each element.

The space complexity of this solution is O(1), which means it uses a constant amount of additional memory, regardless of the input size. This is because the algorithm uses only two additional variables (`smallest` and `second_smallest`) to store the smallest and second smallest numbers.

In contrast, the first solution that creates a new list by concatenating sublists has a time complexity of O(n) but a space complexity of O(n) because it creates a new list with a length proportional to the input size.

Understanding time and space complexity is crucial for analyzing the efficiency of algorithms and making informed decisions when choosing the appropriate solution, especially for large input sizes or resource-constrained environments.