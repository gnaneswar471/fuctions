# fuctions
#function calling and define
def hi():
    print("good morning sir")
hi()
OUTPUT:
good morning sir

#Funtion wih parameter
def hi(name):
    print("Hello",name)
hi('vijay')
OUTPUT:
Hello vijay

# functions with returnn value
def add(a,b):
    return a+b
x=int(input())
y=int(input())
result=add(x,y)
print("sum:",result)
OUTPUT:
 5
 6
sum: 11
'''write a program tha carries and return all the arthemtic operations to the code(+,-,*)
pass the constraints ,where all the consrains must e calculted acccordingly as return values
to print by calling same function '''
def arthmatic(a,b):
    return f"sum: {a+b} , diff: {a-b} , mul: {a*b}"
x=int(input())
y=int(input())
print(arthmatic(x,y))
OUTPUT:
Selection deleted
'''write a program tha carries and return all the arthemtic operations to the code(+,-,*)
pass the constraints ,where all the consrains must e calculted acccordingly as return values
to print by calling same function '''
def arthmatic(a,b):
    return f"sum: {a+b} , diff: {a-b} , mul: {a*b} , div: {a/b}"
x=int(input())
y=int(input())
print(arthmatic(x,y))
OUTPUT:
 5
 4
sum: 9 , diff: 1 , mul: 20 , div: 5.0
 def get_name():
     name=input("Enter your name: ")
     return name
     
username=get_name()
print("Welcome ", username)
OUTPUT:
Enter your name:  gopi
Welcome  gopi

def info(name='unknown',age=0):
    print("Name ",name)
    print("Age ",age)
info("vijay",32)
info("namm")
info(age=99)
info()
OUTPUT:
Name  vijay
Age  32
Name  namm
Age  0
Name  unknown
Age  99
Name  unknown
Age  0
def cal(a,b):
    return a+b,a-b,a*b,a/b
a,b=int(input("Enter a value:")),int(input("Enter b value:"))
sum,diff,pro,div=cal(a,b)
print("sum: ",sum)
print("diff: ",diff)
print("product: ",pro)
print("division:",div)
OUTPUT:
Enter a value: 55
Enter b value: 11
sum:  66
diff:  44
product:  605
division: 5.0

def comp(a,b,c):
    return max(a,b,c),min(a,b,c)

a,b,c=int(input()),int(input()),int(input())
maximum,minimum=comp(a,b,c)
print("Maximum number is: ",maximum)
print("Minimum number is: ",minimum)
OUTPUT:
 5
 11
 12
Maximum number is:  12
Minimum number is:  5

def sep(a):
    e,o=0,0
    for i in a:
        if i%2==0:e+=1
        else:o+=1
    return e,o 
a=eval(input("enter num as list type"))
even,odd=sep(a)
print("Even: ",even)
print("odd: ",odd)
OUTPUT:
enter num as list type 10 ,22 ,33 ,44  ,55 ,66 ,77 ,88 ,99
Even:  5
odd:  4

def sep(num):
    e,o=0,0
    for n in num:
        if n%2==0:e+=1
        else:o+=1
    return e,o
n=input("Enter the number with space seperated: ")
n_l=list(map(int,n.split()))
e,o=sep(n_l)
print("Even: ",e)
print("Odd: ",o)
OUTPUT:
Enter the number with space seperated:  10 22 33 44  55 66 77 88 99
Even:  5
Odd:  4

a=int(input())
expo=lambda a:a**a
print(expo(a))
OUTPUT:
 3
27

def arth(a,b):
    def add():return a+b
    def sub():return a-b
    def mul():return a*b
    print("Addition: ",add())
    print("Subtraction: ",sub())
    print("Multiplication: ",mul())
a=int(input("Enter a value:"))
b=int(input("Enter b value:"))
arth(a,b)
OUTPUT:
Enter a value: 1
Enter b value: 2
Addition:  3
Subtraction:  -1
Multiplication:  2

def mul_by(x):
    def inner(n):return x*n
    return inner
times_2=mul_by(2)
times_3=mul_by(3)
print(times_2(5))
print(times_3(10))
OUTPUT:
10
30

x=100
y=10
def display():
    x=22
    print("x =",x)
    print("y =",y)
    print("Locally x+y =",x+y)
display()
y=25
print("x =",x)
print("y =",y)
print("Globally x+y =",x+y)
OUTPUT:
x = 22
y = 10
Locally x+y = 32
x = 100
y = 25
Globally x+y = 125

total=0
allsubjects,average=0,0
def add_subject_marks():
    global total,allsubjects,average
    marks=int(input("Enter marks of a subject :"))
    total+=marks
    allsubjects+=1
    average=total/allsubjects
    return marks
print("Subject1 marks :",add_subject_marks())
print("Subject2 marks :",add_subject_marks())
print("Subject3 marks :",add_subject_marks())
print("Total marks gained by student :",total)
print(f"Percentage of the student for the acadamic is : {average:.2f}%")
OUTPUT:
Enter marks of a subject : 100
Subject1 marks : 100
Enter marks of a subject : 92
Subject2 marks : 92
Enter marks of a subject : 88
Subject3 marks : 88
Total marks gained by student : 280
Percentage of the student for the acadamic is : 93.33%

subject_marks=[]
def add_subject_marks():
    mark=int(input("Enter marks :"))
    subject_marks.append(mark)
    return mark
all_subjects=int(input("Enter number subjects :"))
for i in range(all_subjects):
    print(f"subject {i+1} marks :",add_subject_marks())
print("all subject marks",subject_marks)
print("Total marks :",sum(subject_marks))
print(f"percentage : {sum(subject_marks)/len(subject_marks):.2f}")
OUTPUT:
Enter number subjects : 3
Enter marks : 100
subject 1 marks : 100
Enter marks : 92
subject 2 marks : 92
Enter marks : 88
subject 3 marks : 88
all subject marks [100, 92, 88]
Total marks : 280
percentage : 93.33

fact=1
def factorial(num):
    global fact
    for i in range(1,num+1):
        fact*=i
    return fact
num=int(input("Enter a number"))
if num<0:
    print(f"Can't derive factorial for negative numbers")
else:
    factorial(num)
    print(f"Factorial of {num} is",fact) 
OUTPUT:
Enter a number 6
Factorial of 6 is 720

def factorial(n):
    if n==0 or n==1:return 1
    return n*factorial(n-1)
num=int(input("Enter a value:"))
value=factorial(num)
print(f"factorial of {num} is {value}")
OUTPUT:
Enter a value: 4
factorial of 4 is 24

def sum(n):
    if n==0:return 0
    return n+sum(n-1)
num=int(input("Enter the number"))
print(f"sum of first {num} numbres is {sum(num)}")
OUTPUT:
Enter the number 5
sum of first 5 numbres is 15

def sumn(*args):
    print(args[4])
    return sum(args)
print(sumn(1,2,3,4,5,6,7,8,9,10))
OUTPUT:
5
55

def info(**k):
    for key,v in k.items():print(f"{key}:{v}")
info(name='kana',age=21,cgpa=8.0)
OUTPUT:
name:kana
age:21
cgpa:8.0

def info(**h):
    print(f"kes:{h.values()}")
    for value in h.items():
        print(value)
info(name='kana',age=21,cgpa=8.0)
OUTPUT:
kes:dict_values(['kana', 21, 8.0])
('name', 'kana')
('age', 21)
('cgpa', 8.0)

def fib(n):
    if n<=1:return n
    else:return fib(n-1)+fib(n-2)
num=int(input("Enter no of terms to be printed:"))
for i in range(num):
    print(fib(i),end=" ")
OUTPUT:
Enter no of terms to be printed: 10
0 1 1 2 3 5 8 13 21 34

#sum of n numbers
def dsum(n):
    if n==0:return 0
    return n%10+temp(n//10)
def temp(n):return dsum(n)
num=int(input("Enter a four digit number:"))
print("sum of digits is:",dsum(num))
'''OUTPUT:
Enter a four digit number: 1234
sum of digits is: 10'''

#using nestedd recurion for finding even or odd
def one(n):
    if n==0:return True
  else:return two(n-1)
def two(n):
    if n==0:return False
    else:return one(n-1)
num=int(input("enter a number:"))
if one(num):print(num,"is a even number")
else:print(num,"is a Odd number")
'''OUTPUT:
enter a number: 8
8 is a even number'''

#nested recursion for assinging number to different names
def A(n):
    if n<=0:return
    print("Gopi",n),B(n-1)
def B(n):
    if n<=0:return
    print("Chintu",n),A(n-1)
num=int(input("Enter a number:"))
A(num)
'''OUTPUT:
Enter a number: 5
Gopi 5
Chintu 4
Gopi 3
Chintu 2
Gopi 1'''

#fibnocci series using recursion
def fib(n):
    if n<=1:return n
    else:return fib(n-1)+fib(n-2)
terms=int(input())
print("fibnnoci series......")
fiba=[fib(i)for i in range(terms)]
print(fiba,end='')
'''OUTPUT:
6
fibnnoci series......
[0, 1, 1, 2, 3, 5]'''

#permutation combinations
'''permuntations of char in tree recursion '''
def permute(s,bucket=''):
    if not s:
        print(bucket)
        return
    for i in range(len(s)):
        ns=s[:i]+s[i+1:]
        permute(ns,bucket+s[i])
text=input("enter a word")
print("posibilities of combinations....")
permute(text)
'''OUTPUT:
enter a word abc
posibilities of combinations....
abc
acb
bac
bca
cab
cba '''

#binary value generaor
def binary(l,b=''):
    if l==0:
        print(b)
        return
    binary(l-1,b+'0')
    binary(l-1,b+'1')
length=int(input("Enter length of string:"))
print("Binary combinations......")
binary(length)
'''OUTPUT:
Enter length of string: 3
Binary combinations......
000
001
010
011
100
101
110
111'''

#usage of head recursion
def head(n):
    if n==0:return
    head(n-1)
    print(n)
num=int(input("Enter a number"))
head(num)
'''OUTPUT:
Enter a number 5
1
2
3
4
5'''

def sumhead(n):
    if n==0:return 0
    return n+sumhead(n-1)
num=int(input())
print(sumhead(num))
OUTPUT:
 5
15

#using of tail recursion
def head(n):
    if n==0:return
    print(n)
    head(n-1)
num=int(input("Enter a number"))
head(num)
OUTPUT:
Enter a number 5
5
4
3
2
1

def tailsum(n,temp=0):
    if n==0:return temp
    return tailsum(n-1,temp+n)
num=int(input())
print(tailsum(num))
OUTPUT:
 5
15
