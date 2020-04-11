# Python-Basics
Made while learning Python with freecpdecamp.org

"""
Started FreeCodeCamp PythonTutorial since Thu Apr  2 16:12:43 2020

@author: Bishal Python Adhikari
Day 1
"""
#Variables
"""
name="Bishal Adhikari"
age=19
num=6

"""
#math module/same as library in C
"""
from math import *

print(35.56*2)
print(pow(num,3))
print(max(5,6))
print(round(num))
print(sqrt(num))
print(pow(num,3))

"""
#string concatenation
"""
print("Hello,"+name+" how are you?")
print("I have been here in this chaotic world since "+str(age)+".")
print(name.replace("Bishal","Madhav"))

favourit=input("Enter your favourite language:")
version=input("Which version?:")

print("You love "+favourit " "+ version)

"""
#calculator 
"""
x=input("First number:")
y=input("Last number:")

sum_ = int(x) + int(y)  #can't add decimal numbers
sum_=float(x) + float(y) #add any number
print(sum_)

"""
#So called MadLib,s game:Nepalthon version
"""
animal = input("Kun Janawar ku Masu manparxa?:")
relation = input("Tapai sangai baseko manxe lai k vanera bolaunuhunxa?:")
place = input("Kun thau ramailo lagxa?:\n")

print(animal + " maarna")
print(" jau na " + relation)
print(place+ " ma")

"""
#lists

"""
countries = ["Nepal","India","China","Bhutan","Pakistan"]
#index:        0        1       2        3         4

print(countries) 
print(countries[1])
print(countries[-1])  # -n means n^th element backwards:China in this case
print(countries[1:])  #all elements after countries[1]
print(countries[1:4]) #elements feom index 1 to 4

countries[3] = USA    

"""
#list functions
""" 

countries = ["Nepal","India","China","Bhutan","Pakistan"]
cases =[5,1900,81000,"Unknown",2100]

cases.append(2000)
print(cases)

cases.extend(countries)
print(cases)

cases.remove("Unknown")
print(cases)

index = cases.index("Nepal")
print(index)

countries.insert(3,"SriLanka")
print(countries)

countries.sort()
print(countries)
#cases.sort()              doesn't support for lists with both numbers and strings
#print(cases)

countries = ["Nepal","India","China","Bhutan","Pakistan","Nepal","Maldives"]
count =countries.count("Nepal")
print(count)
count=countries.count("Maldives")
print(count)

countries.pop()
print(countries)

cases.clear()
print(cases)

cases.reverse()
print(cases)

countries_duplicate = countries.copy()
print(countries_duplicate)

"""
#video paused at 1:18:58 //continuing tomorrow
#Day 2

#tuples
"""
point = (2,8)
print(point[1])
  # point[1]= 7        error : tuples can't be modified
points = [(2,8),(5,6),(2,9)]

"""
#Functions
"""
def greeting_func():
    msg = input("Your name:")
    print("Hello,"+msg+" what are you doing here?")

greeting_func()

def greeting_func(name,relation):
    print("Hello,"+name+" "+relation+" what are you doing here?")
 
greeting_func("Gaurav","vai")

def sqre(num):
    return num*num

sqre(5)                 
print(sqre(5))
result = sqre(5)
print(result)

"""
#Statements
"""
is_male =False
is_fat = True

if is_male and is_fat:
    print("Hey fat boy!")

elif(not(is_male) and is_fat):
    print("You,Hey you potato girl!")

else:
    print("Hey You thin girl!")

def max(a,b,c):
    if((a>b) and (b>c)):
        return a
    elif((b>a) and (b>c)):
        return b
    else:
        return c

print(max(3,1,8))

"""
#Better Calculator
"""
x=input("1st operand:")
y=input("2nd operand:")
operator=input("Enter the operator:")

x = float(x)
y = float(y)

def calculator(a,b):
    if operator == "+":
        return a+b
    elif operator == "-":
        return a-b
    elif operator == "*" :
        return a*b
    elif operator == "/" and b != 0:
        return a/b
    else:
        return "Invalid Operand/s or Operator"

print("Result = "  + str(calculator(x,y)))

"""

#Dictionaries
"""
funny = {                #declaration
    1 : "Aape",          #Assignment
    2 : "Aanand",
    3 : "Babu",
    4 : "Babar",
    5 : "Maddy",
    6 : "Vivek",
    7 : "Pyakuli",
    "Genius" : "Bishal",
    "Smart" : "Madhav",
    "Intelligent" : "Madan",
    "Politician" : "Sagar",
    "Singer" : "Surya",
    "Playful" : "Kundan"
    }
print(funny.get("Genius"))             #Acessing
print(funny["Intelligent"])            #ALternative way
print(funny.get("Silly" , "Roshan"))
print(funny[5])

"""
#A Python Guessing Game

"""
secret = "JUMANJI"
name = input("Enter a username:")
guess = ""
count = 3

print("\n\nWelcome "+name+".Here begins the guessing game.")
print("The password of the vault of diamonds"),
print("is a secret.Guess the PASSWORD and diamonds worth \n trillions of dolars is yours.")

while guess != secret and count >= 0:
        
    if count == 3:
        print("\n "+str(count)+" chance/s remaining.")
        print("\nHint:It is an adventure game!!Once u r into it,very difficult to get out of it.Find it.")
        
    elif count == 2:
        print("\n"+str(count)+" chance/s remaining.")
        print("\nHint:Come on! It starts from letter 'J'")
        
    elif count == 1:
        print("\n"+str(count)+" chance/s remaining.")
        print ("\nHint:It ends with letter 'I'")
           
    elif count == 0:
        print("\nGAME OVER")
        break
        
    guess = input("Enter PASSWORD:")
    guess = guess.upper()
    count = count - 1
    
if guess == secret:    
    print("\nMajesty!You are the greatest of all,you won these diamonds..")
    print("!!! YOU WON !!!")

"""
#for loop
"""

for letter in "Encyclopedia":
    print(letter)

for i in range(1,10):
    print(i)

countries = ["China","Bangladesh","India","Nepal"]
for country in countries:
    print(country)

for index in range(len(countries)):
    print(countries[index])

#can loop through any collections
print("Even numbers less than 20:")  
for i in range(1,20):    
    if i%2 == 0 :
        print(i)

#For loop inside function

def factorial(num):
    ans = 1
    for i in range(1,num+1):
        ans = ans * i
    return ans

num = int(input("Factorial of:"))
print(factorial(num))
        
"""
#2D lists and nested loops

"""
matrix1 = [
     [1,2,3],
     [4,5,6],
     [2,4,7],  
    ]
print(matrix1[0][2])

for row in matrix1:
    for col in row:
         print(col)
"""
#Building a translator
"""

def translate(phrase):
    translated = ""
    
    for letter in phrase:
        if letter in "AEIOUaeiou":
            translated = translated + "p"
        else :
            translated = translated + letter
    return translated
            
phrase = input("Enter a phrase:")
print(translate(phrase))

"""

#try  except block

"""
num = int(input("Enter  a number:"))  
print(num)

#if intered any data except int type,program will crash.

try:
    num = int(input("Enter a number:"))
    print(num)
except:
    print("INvalid")
"""    
"""
try:
    value = 5/0
    num = int(input("Enter a number:"))
    print(num)
 except ZeroDivisionError as err :
    print(err)
except ValueError as err:
    print(err)
 
"""

#file handling
"""
students_file = open("students.txt","r")    #similar as in C (r,w,a,r+,a+,w+)
 
print(students_file.readable())              #.readable() returns true or false
print(students_file.readline())              #reads a line from where the cursor curren
print(students_file.readlines())        #stores each line as an element of a list starting from the cursor
print(students_file.read())                  #reads all and move cursor to eof

students_file.close()


file = open("students.txt","a+")

file.write("\nManish - MBBS")
for line in file.readlines():
    print(line)

file.close()

"""

#classes and objects
'''
#Codes inside quotes are written in a file named class_example.py
# which works as a modue from which class Student is imported in actual code
#as done further below

class Student:                  
    def _init_(self,name,program,period,gpa,is_qualified):
        self.name = name
        self.program = program
        self.period = period
        self.gpa = gpa
        self.is_qualified = is_qualified
 
'''

"""
from class_example import Student           

student1 = Student("BIshal","BIE","Y1S1",3.6,True)
student2 = Student("Madhav","BIE","Y1S1",3.7,True)
student3 = Student("Sanjaya","BE on Civil","Y2S1",3.74,True)

print(student1.name)
print(student2.period)
print(student3.gpa)

"""

#MCQ [Multiple Choice Quiz]

#Object Functions
"""
from class_example import Student


student1 = Student("BIshal","BIE","Y1S1",3.2,True)
student2 = Student("Madhav","BIE","Y1S1",3.45,True)

print(student1.name)
print(student2.honor())     

"""   
