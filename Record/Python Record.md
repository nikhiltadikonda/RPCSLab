# Python Record
#### 1. Write a PHP script to demonstrate any 5 string functions
```php
<?php
echo strlen("Hello world!");
echo "<br>";
echo str_word_count("Hello world!");
echo "<br>";
echo strrev("Hello world!");
echo "<br>";
echo strpos("Hello world!", "world");
echo "<br>";
echo str_replace("world", "Dolly", "Hello world!");
?>
```
#### 2. Write a PHP script to demonstrate indexed and associative arrays
```php
#Indexed Arrays
<?php
$songs = array("Classic", "Jazz", "Retro");
echo "I like " . $songs[0] . ", " . $songs[1] . " and " . $songs[2] . ".";
echo "<br>";
?>

#Associative Arrays
<?php
$score = array("Kohli"=>"99", "Steve Smith"=>"50", "Dhoni"=>"100");
echo "Dhoni Scored " . $score['Dhoni'] . " runs.";
echo "<br>";
?>
```
#### 3. Write a python program that takes input number as n and generate n prime numbers
```py
import math

def is_prime(x):
    for i in range(2, math.sqrt(x)+1):
        if(x % i == 0):
            return False
    return True

print(", ".join([str(i) for i in range(2, int(input("Enter a Number: "))+1) if is_prime(i)]))
```
#### 4. Write a python program that demonstrates list methods
```py
#Append
a = ["bee", "moth"]
a.append("ant")
print(a)

#Insert
a.insert(4, "fly")
print(a)

#Clear
a.clear()
print(a)
a = ["bee", "moth","bee"]

#Count
print(a.count("bee"))

#sort
a.sort()
print(a)
```
#### 5. Demonstrate Dictionary methods in python
```py
sample={
    1:"Hello",
    2:"World",
    3:"Thor"}
print(sample)

print('\n',sample[1],sep="")

print('\n',sample.get(1),sep="")

#Add Element to a Dictioanry 
sample[4]="Thunder"
print(sample)

for x in sample:
    print(x)

#print values
for x in sample.values():
    print(x)

#print key-value pairs
for x,y in sample.items():
    print(x,':',y)

#find whether a value is present in a dictionary or not
if 1 in sample:
    print(sample.get(1))

print(len(sample))
```
#### 6. Demonstrate Set methods in python
```py
a=set([i+1 for i in range(10)])
print(a)

print(1 in a)

a.add(11)

a.update([12,13])
print(a)

print(len(a))

fsa=frozenset(a)
print(fsa)
for i in fsa:
    print(i,end=" ")
```
#### 7. Demonstrate Tuple methods in python
```py
tupdemo=tuple([i+1 for i in range(10)])
print(tupdemo)

#Tuple Comprehension
print(tupdemo[2:5])

print(tupdemo[-8:-1])

print(tupdemo[::-1])

#Add Element in a Tuple
x=list(tupdemo)
x.append(11)
tupdemo=tuple(x)
print(tupdemo)

for x in tupdemo:
    print(x,end=' ')

if 1 in tupdemo:
    print("\nFound it..!")

print(len(tupdemo))

#create a one item tuple
onetup=("Hello",)
print(onetup)

tupdemo=tupdemo+onetup
print(tupdemo)
```
#### 8. Write a python program to implement list comprehension
```py
#List Comprehension
#program to generate an odd list of numbers
odd=[i for i in range(int(input('Enter Range Value'))+1) if i%2!=0]
print("List Generated: ",odd)
```
#### 9. Write a python program that demonstrates try , except and finally using file operations
```py
try:
    f=open('sample.txt','w')
    print("Welcome",file=f)
    f.write("Line 2")
    print(f.read())
    f.close()
except:
    print("Error Occured")
finally:
    print("Finally Block Here")
```
#### 10. Write a python program to implement single and multilevel inheritance
```py
#Single Inheritance
class Person(object): 
    def __init__(self, name): 
        self.name = name

    def getName(self): 
        return self.name 

    def isStudent(self): 
        return False

class Student(Person):

    def isStudent(self): 
        return True

emp = Person("Student1")
print(emp.getName(), emp.isStudent()) 
   
emp = Student("Student2")
print(emp.getName(), emp.isStudent()) 

#Multilevel Inheritance
class Base(object):
    def __init__(self, name): 
        self.name = name

    def getName(self): 
        return self.name

class Child(Base): 

    def __init__(self, name, age): 
        super(Child,self).__init__(name) 
        self.age = age

    def getAge(self): 
        return self.age 
 
class GrandChild(Child): 

    def __init__(self, name, age, address): 
        super(GrandChild,self).__init__(name, age) 
        self.address = address 

    def getAddress(self): 
        return self.address         

g = GrandChild("Geek1", 23, "Noida")   
print(g.getName(), g.getAge(), g.getAddress()) 
```
#### 11. Write a python program that demonstrates polymorphism using OOPS concepts
```py
class Tesla(): 

     def type(self): 
       print("Car")

     def use(self):
       print("Driving")

class Apple():

     def type(self): 
       print("Phone")
 
     def use(self): 
       print("Communication") 
      
def func(obj):
       obj.type() 
       obj.use()
        
obj_tesla = Tesla() 
obj_apple = Apple() 
func(obj_tesla) 
func(obj_apple)
```
#### 12. Write a python program that implements decorators in functions
```py
def temperature(t):
    def celsius2fahrenheit(x):
        return 9 * x / 5 + 32

    result = "It's " + str(celsius2fahrenheit(t)) + " degrees Farenheit" 
    return result

print(temperature(int(input('Enter Temperature in Celsius: '))))
```
#### 13. Write a python program to read write and display contents of CSV files
```py
import csv

with open('names.csv','w',newline='') as csvwritefile:
    fieldnames=['fname','lname']
    writer=csv.DictWriter(csvwritefile,fieldnames=fieldnames)
    
    writer.writeheader()
    writer.writerow({'fname':'Ben','lname':'Stokes'})
    writer.writerow({'fname':'Elon','lname':'Musk'})
    writer.writerow({'fname':'Nikhil','lname':'Tadikonda'})

print("CSV Output:")

with open('names.csv','rt') as csvreadfile:
    reader=csv.DictReader(csvreadfile)
    for row in reader:
        print(row)
```
#### 14. Design a Sample Django App
## Write your own steps to Design a Django App as demonstrated in the Lab. Click [HERE](https://github.com/nikhiltadikonda/PYCTLab/blob/master/Python%20Files/29-02-2020/projects_django.pdf) for Documentation
#### 15. Design a Sample ReactJS App
## Added Later