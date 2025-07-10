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
