# Index
1. What are functions ?
2. Function defintion
3. Scopes
    a. Global
    b. Local 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. What are functions ?
 - A function in Python is a block of reusable code designed to perform a specific task
 - Functions help :
     a. Organize code
     b. Reduce redundancy, and
     c. Make programs easier to read and maintain
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# II. Function definition
  - Syntax:
def function_name(parameters):
    """Optional docstring to describe the function."""
    # Function body
    return result  # Optional

### Ex 1. No argument function
def display():
    print('Hello World!')

display()

### Ex 2. Single argument function
message = input("Enter the message you want to display: ")

def display(m):
    print(m)

display(message)

### Ex 3. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Scope
1. Global
2. Local
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
