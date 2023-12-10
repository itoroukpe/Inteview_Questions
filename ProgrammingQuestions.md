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
