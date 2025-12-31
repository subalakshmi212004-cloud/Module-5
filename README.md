# Constructors in Python: Welcome Message with Student Name
🎯 Aim
```
To write a Python program that creates a Student class with a default constructor and a method to display a welcome message along with the student’s name provided by the user.
```
🧠 Algorithm
```
1.Get user input: Accept the student's name from the user.
2.Define the class: Create a class Student with a default constructor (__init__).
3.Default Constructor: In the constructor, assign the user input (student name) to an instance variable self.a.
4.Display Message: Define a method show that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5.Execute the Program: Instantiate the Student class and call the show method.
```
🧾 Program
```  
name = input()


class Student:
   
    def __init__(self):
        self.a = name  
    
  
    def show(self):
        print("This is non-parameterized constructor")
        print("Hello", self.a)


s = Student()   
s.show()
```
Output

<img width="1155" height="232" alt="530068553-895dcb92-f9a0-4db7-b248-8d482cfbdb48" src="https://github.com/user-attachments/assets/e971a62b-0348-44e5-9468-289b6759672c" />

Result
Thus , the program has been executed succesfully.

Destructor in Python
This project demonstrates how to implement a destructor in Python using a simple class.

🚀 Overview
```
The program defines a class Demo with:

1.A constructor __init__ that initializes an instance variable and prints a message.
2.A destructor __del__ that prints a message when the object is destroyed.
```
🧠 Algorithm
```
1.Define a class named Demo.
2.Inside the class, define the __init__ method:
 Initialize an instance variable status with the value "Alive".
 Print the value of status.
3.Define the __del__ method:
 Print a message indicating the object is being destroyed.
4.Outside the class:
 Create an instance of the Demo class.
 Delete the object using the del keyword.
```
##Program
```
class Demo:   
    def __init__(self):
        self.status = "Alive"
        print(self.status)


    def __del__(self):
        print("The object no longer exists")


obj = Demo()  
del obj
```       
🧪 Output

<img width="717" height="147" alt="530069069-9c626520-2a2e-44d9-955f-d43960c7dd25" src="https://github.com/user-attachments/assets/bc996101-4e77-49cf-8af4-0ae6d1b9942a" />


Result
Thus , the program has been executed succesfully.

Hierarchical Inheritance in Python
```
This Python project demonstrates Hierarchical Inheritance using a base class Details and two derived classes Employee and Patient. The program collects and displays details for both employees and patients.
```
🎯 Aim
```
To write a Python program that uses Hierarchical Inheritance to input and display Employee and Patient details.
```
📘 Description
```
1.Base Class: Details

 *Stores common attributes: name, age
 *Provides methods: getName(), getAge()
2.Derived Class 1: Employee

*Inherits from Details
*Adds: employee_id, department
*Method: getEmployeeDetails()
3.Derived Class 2: Patient

 *Inherits from Details
*Adds: patient_id, disease
*Method: getPatientDetails()
```
🧠 Algorithm
```
Create base class Details with common attributes.
Create Employee class extending Details, adding employee-specific data.
Create Patient class extending Details, adding patient-specific data.
Get user input for employee and patient data.
Display collected information using class methods.
```
Program
```

class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def getName(self):
        return self.name

    def getAge(self):
        return self.age


class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age)
        self.employee_id = employee_id
        self.department = department

    def getEmployeeDetails(self):
        return (
            f"Employee Name: {self.getName()}, "
            f"Age: {self.getAge()}, "
            f"Employee ID: {self.employee_id}, "
            f"Department: {self.department}"
        )


# Derived Class 2
class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease

    def getPatientDetails(self):
        return (
            f"Patient Name: {self.getName()}, "
            f"Age: {self.getAge()}, "
            f"Patient ID: {self.patient_id}, "
            f"Disease: {self.disease}"
        )


name=input()
age=int(input())
employee_id=int(input())
department=input()
employee = Employee(name,age,employee_id,department)
name=input()
age=int(input())
patient_id=int(input())
disease=input()
patient = Patient(name,age,patient_id,disease)


print(employee.getEmployeeDetails())
print(patient.getPatientDetails())
```
Sample Output

<img width="747" height="83" alt="530070606-d4047ee0-d80d-4f15-9a11-f0a8d14b6c85" src="https://github.com/user-attachments/assets/fb6f3081-308b-489b-8530-2770105aa4ba" />

Result
Thus , the program has been executed succesfully.

Multilevel Inheritance Example in Python
```
This Python project demonstrates the concept of Multilevel Inheritance to collect and display the name, age, and location of a person.
```
🎯 Aim
```
To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.
```
🧠 Algorithm
```
Parent Class

__init__(name) initializes the name attribute.
getName() returns the name.
Child Class (inherits Parent)

__init__(name, age) initializes name using super() and adds age.
getAge() returns the age.
Grandchild Class (inherits Child)

__init__(name, age, location) initializes name and age using super() and adds location.
getLocation() returns the location.
Input & Output

Take user input for name, age, and location.
Create an instance of Grandchild.
Print all details using class methods.
Program

class Parent:
    def __init__(self, name):
        self.name = name

    def getName(self):
        return self.name



class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

    def getAge(self):
        return self.age


class Grandchild(Child):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location

    def getLocation(self):
        return self.location



name = input()
age = int(input())
location = input( )


obj = Grandchild(name, age, location)


print("\n--- Details ---")
print("Name:", obj.getName())
print("Age:", obj.getAge())
print("Location:", obj.getLocation())
```
Sample Output

<img width="458" height="122" alt="530073701-467e4618-b91c-4c8e-acc3-09e876b56a62" src="https://github.com/user-attachments/assets/5bb1fc3e-822b-4c57-868d-8b90896a69a1" />

Result
Thus , the program has been executed succesfully.

Arithmetic Operations Using Multiple Inheritance in Python
```
This Python program demonstrates multiple inheritance by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.
```
🎯 Aim
```
To write a Python program to calculate Add, Sub & Division using Multiple Inheritance.
```
🧠 Algorithm
```
1.Define Calculation1 class
 Contains Summation(a, b) method to return the sum of two numbers.
2.Define Calculation2 class
Contains Subtraction(a, b) method to return the difference of two numbers.
3.Define Derived class
 Inherits from both Calculation1 and Calculation2.
 Contains Division(a, b) method to return the division result.
4.Input
 Prompt the user to enter two numbers.
5.Process
 Create an object of the Derived class.
 Call Summation, Subtraction, and Division methods.
6.Output
 Display the results of the three operations.
💻 Program
```class Calculation1:
    def Summation(self, a, b):
        return a + b



class Calculation2:
    def Subtraction(self, a, b):
        return a - b


class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b == 0:
            return "Division by zero not allowed"
        return a / b



num1 = int(input())
num2 = int(input())


obj = Derived()

sum_result = obj.Summation(num1, num2)
sub_result = obj.Subtraction(num1, num2)
div_result = obj.Division(num1, num2)


print("\nResults:")
print("Addition:", sum_result)
print("Subtraction:", sub_result)
print("Division:", div_result)
```
Output Example
<img width="306" height="80" alt="530074534-b33be150-114d-4e2d-bfac-ad42ae17d65b" src="https://github.com/user-attachments/assets/c15ead47-a61d-45ae-b5ba-3c3bc321af98" />


Result
Thus , the program has been executed succesfully.
