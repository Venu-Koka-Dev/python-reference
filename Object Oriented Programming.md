# Index
1. What is Object oriented programming ?
2. Object(Instance) Vs Class
3. Defining a Custom class (data structure)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. What is Object oriented programming ?
 - Object-Oriented Programming (OOP) is a programming paradigm
 - It structures software design around objects, which are instances of classes
 - Python is an Object-oriented language
 - It supports OOP principles such as :
    1. Encapsulation - principle of restricting direct access to some data and methods to prevent unintended modifications
    2. Inheritance
    3. Polymorphism
    4. Abstraction
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# II. Object (Instance) Vs Class

## What is a class ?
 - A class is a blueprint for creating objects
 - It defines properties (variables) and behaviors (methods)

## What is an object(instance) ?
 - An object is an instance of a class that encapsulates data (attributes) and behavior (methods)

## Analogy to understand 
 - A class is like a blueprint for a building
 - Whereas buildings are the objects of that class
 
## Predefined classes and objects
name = "Venu"           # str 
age = 40                # int
height = 6.2            # float
isAdult = True          # bool
marks = [60, 70, 80]    # list
personalInfo = {        # dict
 "fName": "Venu",
 "lName": "Koka",
 "email": "venu@gmail.com"
}
 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Defining a Custom class (data structure)
- A method is a function but defined inside a class

#### Example 1: Defining a simple class with constructor 
class PythonStudent:
    def __init__(self, fName, lName, s_age):
        self.firstName = fName
        self.lastName = lName
        self.age = s_age

    def displayFullName(self):
        return self.firstName + " " + self.lastName
        
    def isAdult(self):
        if self.age > 18:
            return True
        else:
            return False
            
    def greet(self):
        return "Hello!! " + self.firstName  

    def greet(self, message):
        return message + " " + self.firstName  
            

student1 = PythonStudent("Vivek", "Madereddi", 27)     // Instantiation (creating an object)
student2 = PythonStudent("Anil", "Kethu", 12)

print(student1.displayFullName())
print(student1.isAdult())
print(student2.isAdult())
print(student1.greet("Good morning!!"))

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# IV. Encapsulation
  - Encapsulation is the principle of restricting direct access to some data and methods to prevent unintended modifications.
  - Python doesn't support any explicit access modifiers but has a convention for: Public, Protected, and Private Members
     a. Public                  : Accessible from anywhere.
     b. Protected (_variable)   : Suggests restricted access (convention-based)
     c. Private (__variable)    : Not directly accessible from outside the class (rule-based)

#### Example:
class BankAccount:
    def __init__(self, name, account_number, balance):
        self.name = name                        # Public
        self.account_number = account_number    # Public
        self._balance = balance                 # Protected
        self.__pin = 1234                       # Private

    def deposit(self, amount):
        self._balance += amount

    def get_balance(self):
        return self._balance


account = BankAccount("Venu", "123456", 1000)   # Instantiation (Object creation step)
print(account.name)                             # (RECOMMENDED) Public property is Accessible
print(account.account_number)                   # (RECOMMENDED) Public property is Accessible
print(account._balance)                         # (NOT RECOMMENDED) Protected property can also be accessed but do not do it like this
print(account.__pin)                            # (NOT ALLOWED) Private property is not accessible from outside the class and it will raise an AttributeError

print(account.get_balance())                    # (SOLUTION) Accessing a protected property

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# V. Inheritance

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------




















