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
    return f"sum: {a+b} , diff: {a-b} , mul: {a*b}"
x=int(input())
y=int(input())
print(arthmatic(x,y))
OUTPUT:
 5
 4
sum: 9 , diff: 1 , mul: 20

