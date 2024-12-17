# Index
1. What are Strings ?
2. F-strings or f-strings
3. Key features of Strings
4. String conversion methods
5. Accessing Strings
6. Slicing techniques
7. String Operations
    a. Concatenation
    b. Repetition
    c. Membership Testing
8. String methods
9. 
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
 - Numeric String
   Ex. print("123") 
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
# V. Accessing Strings
 - Using indexing
 - Python supports :
    a. Positive indexing : 0 to length-1
    b. Negative indexing : last item is -1
   
### Example 1 : Simple usage of indexing
fName = "Venu"
print(len(fName))

print(fName[3])                     # "u"
print(fName[len(fName) - 1])        # "u"
print(fName[-1])                    # "u"

#Slice of first two characters from the string literal (Using standard while loop)
numOfCharacters = 2
startIndex = 0 

while startIndex < numOfCharacters:
    print(fName[startIndex])
    startIndex = startIndex + 1 

#Slice of first two characters from the string literal (Using for-in loop)
counter = int(input("How many characters do you need from the start of the string: "))
for value in fName:
    if counter == 0:
        break
    else: 
        print(value)

    counter = counter - 1

### Example 2 : Using enumerate() function for extracting index value along with the actual value
fName = "Venu"
for index, value in enumerate(fName):
    print(f'The character at {index} index is : {value}')

    
### Example 3 : Using index value to slice a string
fName = "Venu"
counter = int(input("How many characters do you need from the start of the string: "))
for index, value in enumerate(fName):
    if index < counter:
        print(f'The character at {index} index is : {value}')
    else:
        break


### Example 4 : Using Slicing techniques - varName[start:end:step]
fName = "Venu"
counter = int(input("How many characters do you need from the start of the string: "))
print(fName[:counter])

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VI. Slicing techniques
Syntax:  varName[start:end:step]
1. Default value of start : 0
2. Default value of end : length - 1
3. Default value of step : 1
4. All values are optional
5. Value at end index is excluded
6. Value at start inex is included

### Example 1: To get all values from a string
fName = "Venu"
print(fName[::])

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------  
# VII. String Operations
a. Concatenation / Appending
Note: + is an overloaded operator (Addition operator & Concatenation operator)

fName = "Venu"
lName = "Koka"
print("Mr." + fName + " " + lName)  

b. Repetition
Note: * is also an overloaded operator (Multiplication operator & Repetition operator)

fName = "Venu"
print(fName * 3)

c. Membership Testing (Using in and not in operators)
s = "Python"
print('Py' in s)         # True
print('Java' not in s)   # True
print('y' in s)          # True
print('x' in s)          # False
print('x' not in s)      # True
print("Py" in s)         # True (values should be continuous)
print("Pt" in s)         # False 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VIII. String Methods
1. str.lower()	         : Converts all characters to lowercase [Original value is untouched]
2. str.upper()	         : Converts all characters to uppercase [Original value is untouched]
3. str.title()	         : Converts the first character of each word to uppercase [Original value is untouched]
4. str.strip()	         : Removes leading and trailing whitespaces [Original value is untouched]
5. str.replace(old, new) : Replaces all occurrences of old with new
6. str.split(delim)	     : Splits the string into a list using delim as a delimiter
7. str.join(iterable)	 : Joins elements of iterable with the string as a separator
8. str.find(sub)	     : Returns the lowest index of sub in the string (or -1 if not found)
9. str.isdigit()	     : Returns True if all characters are digits
10. str.isalpha()	     : Returns True if all characters are alphabetic
