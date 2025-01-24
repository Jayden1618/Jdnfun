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

############
A=[[10,20,30], [40,50,60], [70,80,90]]

print("A")

for r in A:

for c in r: print (c,end = "")

print()

#Row-wise Sum

print()

print("Sum of all elements Row-wise:")

for i in range (3):

sum=0

for j in range (3): sum=sum+A[i][j] print("Sum of Row",i," is:", sum)

#Column-wise Sum

print()

print("Sum of all elements Column-wise:")

for i in range (3):

sum=0

for j in range (3): sum=sum+A[j][i] print("Sum of Column", i," is:", sum)

#Sum of all diagonal elements.

sum=0

for i in range (3):

for j in range (3): if(i==j): sum=sum+A[i][j]

print()

print("Sum of all diagonal elements is: ",sum)
print()

print("Operations on Two Matrices:") A=[[10,20,30], [40,50,60], [70,80,90]]

print("A: ")

for rin A:

for c in r:

print (c,end= "")

print()

print()

B=[[1,0,0], [0,1,0], [0,0,1]]

print("B: ")

for rin B:

for c in r:

print (c, end = "")

print()

print()

C=[[0,0,0], [0,0,0], [0,0,0]]

#Addition of Two Matrices

for i in range (3):

for j in range (3):

C[i][j]=A[i][j]+B[i][j]

print("A+B:")

for r in C:

for c in r:

print (c, end = "")

print()

print()

#Multiplication of Two Matrices

M=[[0,0,0], [0,0,0], [0,0,0]]

for i in range (3):

for j in range (3):

sum=0

for k in range (3):

sum=sum+A[i] [k] *B[k] [j]

M[i][j]=sum

print("A*B:")

for rin M:

for c in r:

print (c, end = "")

print()
______________

A = [10, 21, 30, 45, 50]
print("A =", A)

n = len(A)
print("Total number of elements in A =", n)

sum = 0
for x in range(n):
    sum = sum + A[x]
print("Sum of all Elements of A =", sum)

max_n = max(A)
print("Maximum Element =", max_n)

min_n = min(A)
print("Minimum Element =", min_n)

even_n = 0
odd_n = 0
for x in range(n):
    if A[x] % 2 == 0:
        even_n = even_n + 1
    else:
        odd_n = odd_n + 1
print("Total Even numbers in A =", even_n)
print("Total Odd numbers in A =", odd_n)

num = int(input("Enter the number to be searched: "))
flag = 0
for x in A:
    if num == x:
        flag = 1
        break

if flag == 1:
    print("The element is present in the array A.")
else:
    print("The element is not present in the array A.")
