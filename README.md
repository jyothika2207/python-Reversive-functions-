# python-Reversive-functions-
# Factorial using Recursion
def factorial(n):
    if n==0 or n==1:
        return 1
    return n*factorial(n-1)
num=int(input("enter the value:"))
value=factorial(num)
print(value)


========OUTPUT===========
enter the value: 5
120
