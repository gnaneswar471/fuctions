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
