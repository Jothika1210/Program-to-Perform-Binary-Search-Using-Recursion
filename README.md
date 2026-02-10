# Program-to-Perform-Binary-Search-Using-Recursion
def binarySearch(numbers, low, high, x):
    if high >= low:
        mid = low + (high - low) // 2

        if numbers[mid] == x:
            return mid
        elif numbers[mid] > x:
            return binarySearch(numbers, low, mid - 1, x)
        else:
            return binarySearch(numbers, mid + 1, high, x)
    else:
        return -1


numbers = [9, 4, 6, 7, 2, 1, 5]

# Binary search requires sorted list
numbers.sort()

x = int(input("Enter the element to search: "))

result = binarySearch(numbers, 0, len(numbers) - 1, x)

if result != -1:
    print("Search successful, element found at position", result)
else:
    print("The given element is not present in the array")
output
Enter the element to search: 7
Search successful, element found at position 5
