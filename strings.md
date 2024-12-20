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
 - String methods to manipulate and analyze string objects
 - Methods are special functions called on a member/object/instance of a Class/Type
 - (API) Application Programming Interface
    
 1. str.lower()	                           : Converts all characters to lowercase [Original value is untouched]
 2. str.upper()	                           : Converts all characters to uppercase [Original value is untouched]
 3. str.title()	                           : Converts the first character of each word to uppercase [Original value is untouched]
 4. str.strip()	                           : Removes leading and trailing whitespaces [Original value is untouched]
 5. str.replace(old, new)                  : Replaces all occurrences of old with new
 6. str.split(delim)	                   : Splits the string into a list using delim as a delimiter
 7. str.join(iterable)	                   : Joins elements of iterable with the string as a separator
 8. str.find(sub[, start[, end]])          : Returns the lowest index where the substring is found, or -1 if not found
 9. str.isdigit()	                       : Returns True if all characters are digits
10. str.isalpha()	                       : Returns True if all characters are alphabetic
11. str.capitalize()                       : Returns a copy of the string with the first character capitalized and the rest lowercased
12. str.casefold()                         : Returns a case-folded version of the string (similar to lowercase but more aggressive)
13. str.center(width[, fillchar])          : Centers the string within the specified width using a fill character (default is space)
14. str.count(sub[, start[, end]])         : Counts the occurrences of a substring in the string
15. str.encode(encoding='utf-8', errors='strict') : Returns an encoded version of the string
16. str.endswith(suffix[, start[, end]])   : Returns True if the string ends with the specified suffix
17. str.expandtabs(tabsize=8)              : Replaces tabs (\t) with spaces, using the given tab size
18. str.format(*args, **kwargs)            : Formats the string using placeholders
19. str.format_map(mapping)                : Similar to format(), but uses a mapping object.
20. str.index(sub[, start[, end]])         : Returns the lowest index where the substring is found. Raises ValueError if not found.
21. str.isalnum()                          : Returns True if all characters are alphanumeric.
22. str.isascii()                          : Returns True if all characters are ASCII.
23. str.isdecimal()                        : Returns True if all characters are decimals.
25. str.isidentifier()                     : Returns True if the string is a valid Python identifier.
26. str.islower()                          : Returns True if all characters are lowercase.
27. str.isnumeric()                        : Returns True if all characters are numeric.
28. str.isprintable()                      : Returns True if all characters are printable.
29. str.isspace()                          : Returns True if all characters are whitespace.
30. str.istitle()                          : Returns True if the string is title-cased.
31. str.isupper()                          : Returns True if all characters are uppercase.
32. str.ljust(width[, fillchar])           : Left-justifies the string within the specified width.
33. str.lstrip([chars])                    : Removes leading characters (default is whitespace).
34. str.maketrans(x[, y[, z]])             : Returns a translation table for use with translate().
35. str.partition(sep)                     : Splits the string into three parts: before, separator, and after.
36. str.rfind(sub[, start[, end]])         : Returns the highest index where the substring is found, or -1 if not found.
37. str.rindex(sub[, start[, end]])        : Returns the highest index where the substring is found. Raises ValueError if not found.
38. str.rjust(width[, fillchar])           : Right-justifies the string within the specified width.
39. str.rpartition(sep)                    : Splits the string into three parts: before, separator, and after, starting from the end.
40. str.rsplit(sep=None, maxsplit=-1)      : Splits the string from the right into a list.
41. str.rstrip([chars])                    : Removes trailing characters (default is whitespace).
42. str.splitlines([keepends])             : Splits the string at line breaks.
43. str.startswith(prefix[, start[, end]]) : Returns True if the string starts with the specified prefix.
44. str.swapcase()                         : Swaps the case of all characters.
45. str.translate(table)                   : Applies a translation table to the string.
46. str.zfill(width)                       : Pads the string with zeros on the left to make it the specified width.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# "Venu Rao Koka"
fullName = "veNu rao kOka"   # fullName is an object/member/instance of a class str

listWords = fullName.split(" ");  # ["veNu", "rao", "kOka"]

for index, word in enumerate(listWords):  # word = "rao"  index = 1
    listWords[index] = word.lower()  

# listWords = ["venu", "rao", "koka"]
for index, word in enumerate(listWords):  # index = 0 ; word = "venu"
    listWords[index] = word.capitalize()

print(" ".join(listWords))    # "venu rao koka"
