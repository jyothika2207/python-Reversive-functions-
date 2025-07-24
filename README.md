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



def one(n):
    if n==0:
        return True
    else:
        return two(n-1)
def two(n):
    if n==0:
        return False
    else:
        return one (n-1)
num=int(input("enter a number:"))
if one(num):
    print(num,"is even")
else:
    print(num,"is odd")

    =============OUTPUT==============
    enter a number: 4
      4 is even



def A(n):
    print("Jyothika",n)
    B(n-1)
def B(n):
    if n<=0:
        return
    print("Koliki",n)
    A(n-1)
num=int(input("enter a number:"))
A(num)

=========OUTPUT===============
enter a number: 4
Jyothika 4
Koliki 3
Jyothika 2
Koliki 1
Jyothika 0




# fib on tree recursions 0 1 1 2 3 5 8
def fib(n):
    if n<=1:
        return n
    return fib(n-1)+fib(n-2)
terms=int(input("Enter number of terms to print:"))
print(("fibanacci series....."))
for i in range(terms):
    print(fib(i), end=' ')

    ======OUTPUT=========
    Enter number of terms to print: 8
    fibanacci series.....
     0 1 1 2 3 5 8 13 



# '''permuatations of characters in tree recursions'''
def permute(s,bucket=' '):
    if not s:
        print(bucket)
        return
    for i in range(len(s)):
        ns=s[:i]+s[i+1:]
        permute(ns,bucket+s[i])
text=input("Enter a name/word:")
print("possibilities of combinations....")
permute(text)

======OUTPUT============
Enter a name/word: abc
possibilities of combinations....
 abc
 acb
 bac
 bca
 cab
 cba



# program for binary combinations
 def binary(n, b=' '):
    if n==0:
        print (b)
        return
    binary(n-1, b+'0')
    binary (n-1, b+'1')
length=int(input("enter length of string:"))
print("Binary combinations..........")
binary(length)


====OUTPUT============
enter length of string: 3
Binary combinations..........
 000
 001
 010
 011
 100
 101
 110
 111



# '''tail recursion'''
def head(n):
    if n==0:
        return
    print(n)
    head (n-1)
num=int(input("Enter a number:"))
head(num)

======OUTPUT=======
Enter a number: 5
5
4
3
2
1
