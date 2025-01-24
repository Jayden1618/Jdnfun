see# Jdnfun

stack = []
answer = 0

while answer != 3:
    answer = int(input("1. PUSH\n2. POP\n3. EXIT\t"))
    if answer == 1:
        n = int(input("Enter the number: "))
        stack.append(n)
        print("Stack:", stack)
    if answer == 2:
        n = len(stack)
        if n == 0:
            print("Underflow Situation: The Stack is EMPTY.")
        else:
            elt = stack[n - 1]
            stack.remove(elt)
            print("Element", elt, "is removed.")
            print("Stack:", stack)

_________

def merge_sort(arr):
    #print()
    #print(arr)
    if len(arr) > 1:
        mid = len(arr) // 2  # Finding the mid of the array
        left_half = arr[:mid]  # Dividing the elements into 2 halves
        right_half = arr[mid:]
        #print("Left Half :", left_half)
        #print("Right Half :", right_half)

        merge_sort(left_half)  # Sorting the first half
        merge_sort(right_half)  # Sorting the second half

        i = j = k = 0

        # Copy data to temp arrays L[] and R[]
        while i < len(left_half) and j < len(right_half):
            if left_half[i] < right_half[j]:
                arr[k] = left_half[i]
                i += 1
            else:
                arr[k] = right_half[j]
                j += 1
            k += 1

        # Checking if any element was left
        while i < len(left_half):
            arr[k] = left_half[i]
            i += 1
            k += 1

        while j < len(right_half):
            arr[k] = right_half[j]
            j += 1
            k += 1

        #print("Merged :", arr)

arr = [12, 11, 13, 5, 6, 7]
print("Given array is:", arr)
merge_sort(arr)
print("Sorted array is:", arr)
