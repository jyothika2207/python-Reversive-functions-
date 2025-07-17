# python-Recursive functions-
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

# Sum OF Natural numbers number
def nsum(n):
    if n==0:
        return 0
    return n+nsum(n-1)
num=int(input("enter n:"))
print("sum of first",num,"natural numbers is",nsum(num))

========OUTPUT=========
enter n: 8
sum of first 8 natural numbers is 36


def rstring(s):
    if len(s)==0:
        return s
    return rstring(s[1:])+s[0]
text=input("Enter a word")
print(rstring(text))

=======OUTPUT=========
Enter a word jyothika
akihtoyj


def sumnum(*args):
    print(args[4 ])
    print(args[6])
    return sum(args)
print(sumnum(1,2,3,4,5,6,7,8,9,10))

=========OUTPUT==========

5
7
55




'''Keyword args **kwargs  '''
def info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}:{value}")
info(name='Jyothika', age=19,cgpa=8.5)


==========OUTPUT============
name:Jyothika
age:19
cgpa:8.5


# fibonacci 1 1 2 3 4 5 8 13 21 34 55
def fib(n):
    if n<=1:
        return n
    else:
        return fib(n-1)+fib(n-2)
num=int(input("enter the terms:"))
for i in range(num):
    print(fib(i),end=' ')

    =======OUTPUT===========
    enter the terms: 11
  0 1 1 2 3 5 8 13 21 34 55 




# sum of digits using indirect recursion
  def dsum(n):
    if n==0:
        return 0
    return n%10+temp(n//10)
def temp(n):
    return dsum(n)
num=int(input("enter a 4 digit number:"))
print("sum of digits:",dsum(num))

==========OUTPUT==============
enter a 4 digit number: 3456
sum of digits: 18



