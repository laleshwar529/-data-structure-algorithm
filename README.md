# -data-structure-algorithm
# 1. Reverse an array using stack data structure

def reverse_array(arr):
    stack = []
    # Push all elements onto the stack
    for element in arr:
        stack.append(element)
    # Pop all elements from the stack into a new array
    reversed_arr = []
    while stack:
        reversed_arr.append(stack.pop())
    return reversed_arr

# Example usage
arr = [1, 2, 3, 4, 5]
print("Original Array:", arr)
print("Reversed Array:", reverse_array(arr))

# Output:
# Original Array: [1, 2, 3, 4, 5]
# Reversed Array: [5, 4, 3, 2, 1]


# 2. Match parentheses stored in a string using stack data structure

def is_parentheses_matched(expression):
    stack = []
    for char in expression:
        if char == '(':
            stack.append(char)
        elif char == ')':
            if not stack:
                return False
            stack.pop()
    return len(stack) == 0

# Example usage
expression = "(a + b) * (c + d)"
print("Expression:", expression)
print("Parentheses Matched:", is_parentheses_matched(expression))

# Output:
# Expression: (a + b) * (c + d)
# Parentheses Matched: True


# 3. Calculate the sum of all integer elements in an integer array by implementing a recursive sum function

def recursive_sum(arr, n):
    if n == 0:
        return 0
    else:
        return arr[n - 1] + recursive_sum(arr, n - 1)

# Example usage
arr2 = [5, 10, 15, 20]
print("Array:", arr2)
print("Sum of all elements:", recursive_sum(arr2, len(arr2)))

# Output:
# Array: [5, 10, 15, 20]
# Sum of all elements: 50
