## Programming Questions

#### write a function in python 2 write a function that takes a list of numbers, numbers, and return the largest number in the list. If there are no numbers in the list, return 0. 
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
#### Suppose you are given a binary tree represented as an array. For example, [3,6, 2, 9, -1, 10] represents the following binary tree (where -1 is a non-existent node): Write a function that determines whether the left or right branch of the tree is larger. The size of each branch is the sum of the node values. The function should return the string "Right" if the right side larger and "Left" if the left side is larger. IF the tree has 0 nodes or if the size of the branches are equal, return the empty string. 

```py
def compare_branches(tree):
    def get_branch_sum(index):
        # Helper function to calculate the sum of the branch starting from the given index
        if index >= len(tree) or tree[index] == -1:
            return 0

        left_index = 2 * index + 1
        right_index = 2 * index + 2

        return tree[index] + get_branch_sum(left_index) + get_branch_sum(right_index)

    # Calculate the sum of the left and right branches
    left_sum = get_branch_sum(1)  # Start from the root's left child
    right_sum = get_branch_sum(2)  # Start from the root's right child

    # Compare the sums and return the result
    if left_sum > right_sum:
        return "Left"
    elif right_sum > left_sum:
        return "Right"
    else:
        return ""

# Example usage:
binary_tree = [3, 6, 2, 9, -1, 10]
result = compare_branches(binary_tree)
print(result)

```py
