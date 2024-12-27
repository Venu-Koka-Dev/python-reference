# Index
1. Scopes
    a. Global
    b. Local 
2. What are functions ?
3. Function definition & function calling/execution
4. 
    
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. Scopes
1. Global
   
### Ex 1: 
message = input("Enter the message you want to display: ")   # Scope: Global variable
print(dir())   # ['__annotations__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'message'] 

###
>>> dir()
['__annotations__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__']
>>> __builtins__
<module 'builtins' (built-in)>
>>>import builtins
>>>print(dir(builtins))

3. Local variable
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# II. What are functions ?
 - A function in Python is a block of reusable code designed to perform a specific task
 - Functions help :
     a. Organize code
     b. Reduce redundancy, and
     c. Make programs easier to read and maintain
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Function definition & function calling(execution)
  - General Syntax:
def function_name(parameters):
    """Optional docstring to describe the function."""
    # Function body
    return result  # Optional

  - Parameters are placeholders in the function definition
  - Arguments are actual values passed to the function when it is called

### Ex 1. No argument function
def display():
    print('Hello World!')

display()

### Ex 2. Single argument function (Parameterisation)
message = input("Enter the message you want to display: ")

def display(m):
    print(m)

display(message)

### Ex 3. Multiple arguments function (Parameterisation)
greet = input("Please enter the greeting: ")
name = input("Please enter whom you want to greet: ")
gender = input("Enter F for female or M for male: ")

def display(g, n, gen):
    print(f"{g} {"Mr." if gen == "M" else "Miss."}{n}")

display(greet, name, gender)

### Ex. 4. Importing a function from a module
operations.py[MODULE]
# Author : Uday CH (owner of the module operations.py)
author = "Uday Chodisetti"

def add(v1, v2):
    result = v1 + v2    
    return result
    
def sub(v1, v2):
    return v1 - v2

def mul(v1, v2):
    return v1 * v2

def div(v1, v2):
    return v1 / v2


calculator.py[User]
# Author : Vivek
# Arithmetic Addition operation 
import operations

value1 = int(input("Enter the first number : "))
value2 = int(input("Enter the second number : "))
operation = input("Enter A for addition, S for subtraction, M for multiplication & D for division : ").lower()

if operation == "a":
    result = operations.add(value1, value2)
    print(f"The result of addition of {value1} & {value2} is {result} ")
elif operation == "s":
    result = operations.sub(value1, value2)
    print(f"The result of subtraction of {value1} & {value2} is {result} ")
elif operation == "m":
    result = operations.mul(value1, value2)
    print(f"The result of multiplication of {value1} & {value2} is {result} ")
elif operation == "d":
    result = operations.div(value1, value2)
    print(f"The result of division of {value1} & {value2} is {result} ")
else:
    print("Oops!! Invalid operation entered!!")
    
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
