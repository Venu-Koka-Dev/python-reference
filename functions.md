# Index
1. Scopes
    a. Global
    b. Local 
2. What are functions ?
3. Types of functions - Builtin functions & User defined(Custom) functions
4. Function definition & function calling/execution
5. Required Positional arguments
6. Default Parameters
7.  Variable-Length Arguments
8.  Techniques of function calling - Pass by value, Pass by Reference
    
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
 - API of a function :
     a. Name of the function
     b. Number of arguments/parameters & type(required/default)
     c. Data type of each argument/parameter
     d. Order/Position of each argument/parameter
     e. Return value
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Types of functions 
1. Built-in functions - 

2. User defined functions
   
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# IV. Function definition & function calling(execution)
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
### Ex. 5. Importing a function from a module (More sophisticated version)
operations.py[MODULE]
# Author : Uday CH (owner of the module operations.py)
author = "Uday Chodisetti"

def op(v1, v2, operator):
    if operator == "a":
       result = v1 + v2
       return result
    elif operator == "s":
       result = v1 - v2
       return result
    elif operator == "m":
       result = v1 * v2
       return result
    elif operator == "d":
       result = v1 / v2
       return result
    else:
       return "Not found"

calculator.py[User]
# Author : Vivek
# Arithmetic Addition operation 
import operations


value1 = int(input("Enter the first number : "))
value2 = int(input("Enter the second number : "))
operation = input("Enter A for addition, S for subtraction, M for multiplication & D for division : ").lower()

result = operations.op(value1, value2, operation)

if result == "Not found":
    print("Oops!! Wrong operation input")
else:
    print(f"The result of the operation is {result}")

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# V. Required(Mandatory) positional(order) argument
greet_message = input("Enter the greeting message that you want to print : ")

def display(greet_message):
   print(greet_message)

display(greet_message)   # greet_message is the required positional argument

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VI. Default(Optional) Parameters / Keyword parameters
 - Arguments with default values are optional when calling the function. If omitted, the default value is used
   
# Default optional argument
greet_message = input("Enter the greeting message that you want to print : ")
name = input("Enter the name whom you want to greet :")

def display(greet_message, name = "Guest"):  # name is the default(optional) parameter
   print(f"{greet_message}: {name}")

display(greet_message)



Note: Order within the default arguments not important but must be after positional arguments
def task(message, name, gender = "Male", age = "24"):
    print(f"{message} {gender} {name} with {age} years old")


task("Good morning!", "Vani", age = "30", gender = "Female")

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VII.  Variable-Length Arguments (Varargs)
 - Two types :
   a. *args: For positional arguments of variable length - Note: args is of type tuple

## Ex 1: 
def add(*l):
    result = 0
    for value in l:
       result = result + value    
    return result

result = add(10, 20, 30, 40)

print(result)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VIII. Rules & best practices
1. (Rule) Positional Arguments Must Precede Default Arguments
   Ex. print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
2. (Convention) While calling a function, maintain the exact sequence and use names for named default arguments
## Ex 1 :   
def task(message, name, gender = "Male", age = "24"):
    print(f"{message} {gender} {name} with {age} years old")


task("Good morning!", "Vani", gender =  "Female", age = "40")

3. Mutable Default Arguments Should Be Avoided

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
