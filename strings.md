# Index
1. What are Strings ?
2. F-strings or f-strings
3. Key features of Strings
4. String conversion methods
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. What are Strings 
 - Any sequence of characters (digits, alphabets or special characters)
 - Sequence : order of characters
 - String literal
   Ex. fName = "Venu"
       lname = "Koka"
 - Enclosed in quotes (either single, double, or triple)
   Ex. print("Venu")
       print('Venu')
       print("""Venu""")
       print('''Venu''')
       print('Venu said, "Lets for a walk tomo".')
       print("This is Venu's cricket bat.")
       print("Venu said, \"Lets for a walk tomo\".")
       print('This is Venu\'s cricket bat.')
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------   
# II. F-strings
 -  Formatted string literals
 -  Provide a concise and readable way to embed expressions within string literals

### Ex 1. Readable & Concise
fName = "Venu"
lName = "Koka"

print("The customer's full name is Venu Koka")
print("The customer's full name is", fName, lName)

print(f"The customer's full name is {fName} {lName}")  # Readable
print(F"The customer's full name is {fName} {lName}")  # Readable

print(f'The customer full name is {fName} {lName}')  # Readable
print(F'The customer full name is {fName} {lName}')  # Readable

### Ex 2. Expressions inline/embedded
fName = "Venu"
lName = "Koka"
gender = "M"

prefix = "Mr." if gender == "M" else "Miss."
print("The customer's full name is Mr.Venu Koka")
#print("The customer's full name is", prefix, fName, lName)
print(f"The customer's full name is {prefix}{fName} {lName}")
print(f"The customer's full name is {"Mr." if gender == "M" else "Miss."}{fName} {lName}")

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Key features of Strings
1. Ordered (Sequence) - Strings maintain the order of their characters, allowing for operations like slicing and indexing
2. By defaut, it is an iterable data type - Supports iteration using for..in loop 
Ex. fullName = "Venu Koka"
    for value in fullName:
       print(value)
3. Immutable - cannot be modified after they are created
   i.e. Python strings does not allow for in-place updates
Ex. fName = "Venu"
    fName[0] = "v"   # Syntax Error : not allowed  

Note: Any operation that appears to modify a string in-place will actually return a new string. 
fName = "Venu"
print(fName.lower())   # A new string is returned
print(fName)           # Original value is untouched

4. Supports sequence-specific methods
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# IV. String conversion methods
userID = 452345
userName = str(userID)
print(userName)  # "452345"

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


