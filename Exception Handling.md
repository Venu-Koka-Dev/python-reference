# Index
1. What are Errors ?
2. What are Exceptions ?
3. Handling Excpetions
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. What are Errors ?
 - Two types of Errors in Programming:
    a. Syntax error                     : these errors occur when the Python interpreter encounters something that it doesn’t understand or cannot execute i.e. on violation of Python’s syntax rules
    b. Runtime errors                   : these occur while the program is running and often result in exceptions Ex. DivisionByZeroError
    c. Semantic error / Logical errors  : these errors are not caught by Python interpreter
 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# II. What are Exceptions ?
 - Exceptions are specific types of runtime errors
 - They are objects that Python raises when something goes wrong
 - Examples of pre-defined exceptions:
    a. ZeroDivisionError :	Raised when dividing by zero.
    b. IndexError	       :  Raised when accessing an invalid index of a list or tuple.
    c. KeyError	         :  Raised when a key is not found in a dictionary.
    d. TypeError	       :  Raised when an operation is applied to an inappropriate type.
    e. ValueError	       :  Raised when a function receives an argument of the right type but inappropriate value.
    f. FileNotFoundError :	Raised when a file or directory is requested but doesn’t exist.
    g. ImportError	     :  Raised when an import statement fails.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Handling Exceptions
 - Multiple ways:
    a. Using decision making statements like if..else or ternary operators
    b. Using try..except..else..finally
        - try: Code block where exceptions might occur
        - except: Handles specific exceptions
        - else: Executes if no exception occurs
        - finally: Executes regardless of whether an exception occurred

#### Example 1: Handling runtime errors using if-else conditions & printing meaningful output error messages to the end user
value1 = int(input("Enter the first number:"))
value2 = int(input("Enter the second number:"))

def div(value1, value2):
  return value1 / value2

if value2 != 0: 
  result = div(value1, value2)
  print(result)
else:
  print("Zero is not acceptable for the second number!!") 

#### Example 2: Handling exceptions using try..except blocks
def connectDb(dbServerName, dbUser, dbPassword):
   valid_dbUser = ""
   valid_dbServerName = ""
   valid_dbPassword = ""
   # line 1
   # line 2
   # line 3  
   if isinstance(dbUser, str):
      valid_dbUser = dbUser.strip()
      print("Valid user!!")
   else:
      raise TypeError("Wrong input for dbUser - Expects a string type")
   # line 4
   # line 5  
   print("Connection established to the Database server")

try:
   connectDb("mdc234db ", 2389 , "12345")
   print("Here")
except TypeError as e:
    print(f"A type mismatch occurred: {e}")   
except Exception as e:
    print(f"An error occurred: {e}")

#### Example 3: 
try:
    # Attempt to open the file and read its contents
    file = open("example.txt", "r")
    content = file.read()
except FileNotFoundError:
    # Handle the case where the file doesn't exist
    print("Error: The file was not found.")
except IOError:
    # Handle other I/O errors
    print("Error: An I/O error occurred while accessing the file.")
else:
    # Process the file contents if no exceptions occur
    print("File content successfully read:")
    print(content)
finally:
    # Ensure the file is closed no matter what
    file.close()
    print("File closed.")
    
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
