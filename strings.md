# Index
1. What are Strings ?
2. F-strings or f-strings


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
   
# II. F-strings
 -  Formatted string literals
 -  Provide a concise and readable way to embed expressions within string literals
Ex.
fName = "Venu"
lName = "Koka"

print("The customer's full name is Venu Koka")
print("The customer's full name is", fName, lName)

print(f"The customer's full name is {fName} {lName}")  # Readable
print(F"The customer's full name is {fName} {lName}")  # Readable

print(f'The customer full name is {fName} {lName}')  # Readable
print(F'The customer full name is {fName} {lName}')  # Readable






