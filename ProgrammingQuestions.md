### Programming Question

## write a function in python 2 write a function that takes a list of numbers, numbers, and return the largest number in the list. If there are no numbers in the list, return 0. 
```py
def find_largest_number(numbers):
    # Check if the list is empty
    if not numbers:
        return 0

    # Initialize the largest number with the first element of the list
    largest_number = numbers[0]

    # Iterate through the list to find the largest number
    for number in numbers:
        if number > largest_number:
            largest_number = number

    return largest_number

# Example usage:
numbers_list = [12, 5, 27, 8, 15]
result = find_largest_number(numbers_list)
print("The largest number is:", result)
```
In Python 2, you can use the `unittest` module to write test cases. Here's an example of a test case for the `find_largest_number` function:

```python
import unittest

class TestFindLargestNumber(unittest.TestCase):

    def test_find_largest_number(self):
        # Test case where the list is not empty
        numbers_list = [12, 5, 27, 8, 15]
        result = find_largest_number(numbers_list)
        self.assertEqual(result, 27)

        # Test case where the list is empty
        empty_list = []
        result_empty_list = find_largest_number(empty_list)
        self.assertEqual(result_empty_list, 0)

        # Test case with negative numbers
        negative_numbers = [-5, -8, -2, -1]
        result_negative = find_largest_number(negative_numbers)
        self.assertEqual(result_negative, -1)

        # Test case with repeated numbers
        repeated_numbers = [7, 7, 7, 7]
        result_repeated = find_largest_number(repeated_numbers)
        self.assertEqual(result_repeated, 7)

if __name__ == '__main__':
    unittest.main()
```

In this test case, we have covered scenarios where the list is not empty, the list is empty, there are negative numbers, and there are repeated numbers. The `unittest` module provides assertions like `assertEqual` to check if the actual result matches the expected result. To run the test case, execute the script, and it will run all the test methods in the `TestFindLargestNumber` class.
