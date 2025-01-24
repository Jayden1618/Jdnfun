# Jdnfun

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
