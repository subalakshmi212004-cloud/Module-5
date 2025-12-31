# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
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
## Sample Output
<img width="747" height="83" alt="530070606-d4047ee0-d80d-4f15-9a11-f0a8d14b6c85" src="https://github.com/user-attachments/assets/8bc3a62e-e8c2-4334-bfa0-46e90e83370c" />
##Result:
Thus , the program has been executed succesfully.




