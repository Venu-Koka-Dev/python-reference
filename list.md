# Index
1. What are lists ?
2. Creating/Defining lists
3. Accessing lists
4. Slicing techniques
5. Iterating techniques
6. Mutating lists
7. List methods 
8. List Comprehensions
9. List vs Tuple
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. What are lists ?
 - It is a data structure in
 - It allows us to store multiple values in a single variable
 - These values can be of different data types (integers, strings, floats, objects, etc.) i.e. heterogeneous types
   Ex. my_list = [10, "Python", True, 3.5, [1, 2, 3], { "x": 1, "y": 2 }]
 - (Recommended) Use it to store homogeneous types
   Ex. my_marks = [45, 67, 80, 45]
   Ex. my_products = [{ "id": 1, "productName": "Cricket bat", "productPrice": 5000 }, {}, {}, {}]
 - Ordered: it is a sequence & can be accessed using Indexing (0, 1, 2 . . . )
 - Mutable: In-place modification of the list after its creation (add, remove, or change items)
 - Allows Duplicates
 - Iterable object
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# II. Creating/Defining lists
1. List literal technique 
my_list = []
numbers = [1, 2, 3, 4, 5]                   # List with integers
mixed_list = [1, "Hello", 3.14, True]       # List with mixed data types
nested_list = [[1, 2, 3], ["a", "b", "c"]]  # Nested list (a list inside another list)

2. Using list() function 
my_list = list((10, 20, 30, 40, 50))        # Takes a tuple of items as an argument

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Accessing lists
 - Using Indexing
 - Uses zero-based indexing i.e.the first element is at index 0
 - Lists supports:
    a. Positive indexing &
    b. Negative indexing

## Example 1: Using indices in List
my_marks_list = [10, 20, 30, 40, 50]
first_subject_marks = my_marks_list[0]
second_subject_marks = my_marks_list[1]
last_subject_marks = my_marks_list[len(my_marks_list) - 1]
(or)
last_subject_marks = my_marks_list[-1]

## Example 2: Nested list
nested_list = [
    [1, 2, 3],
    ["a", "b", "c"],
    [True, False]
]

print(nested_list[0][1])  # Output: 2
print(nested_list[1][2])  # Output: c

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# IV. Slicing techniques
 - To retrieve a portion/part of a list 
 - Syntax: my_list[start:stop:step]

## Example 1: Using indices in List
my_marks_list = [10, 20, 30, 40, 50]
my_marks_list[::]                        # [10, 20, 30, 40, 50]
my_marks_list[0:3:1]                     # [10, 20, 30]  because item in the 3rd index is excluded

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# V. Iterating techniques

1. Using while
my_marks = [10, 20, 30, 40, 50]
startIndex = 0
while startIndex < len(my_marks):
  print(my_marks[startIndex])
  startIndex = startIndex + 1

3. Using for..in
my_marks = [10, 20, 30, 40, 50]
for value in my_marks:
  print(value)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VI. Mutating lists
 - Lists are mutable data types i.e. allows in-place updates

## Example 1:
my_list = ["apple", "banana", "cherry"]
my_list[1] = "blueberry"                                          # ['apple', 'blueberry', 'cherry']  Changing an Element

my_list = ["apple", "banana", "cherry"]
my_list.append("orange")                                          # Output: ['apple', 'banana', 'cherry', 'orange']  Adding elements

my_list = ["apple", "banana", "cherry"]
my_list.insert(1, "blueberry")                                    # Output: ['apple', 'blueberry', 'banana', 'cherry']  Inserts an element at a specified index

my_list = ["apple", "banana", "cherry", "banana"]
my_list.remove("banana")                                          # Output: ['apple', 'cherry', 'banana']  Removes the first occurrence of a specified value

my_list = ["apple", "banana", "cherry"]
fruit = my_list.pop(1)                                            # Output: ['apple', 'cherry']   Removes an element by index and returns it
print(fruit)                                                      # 'banana'          

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VII. List methods
1. append()	 : Adds an element to the end of the list	my_list.append(6)
2. insert()	 : Inserts an element at a specific position	my_list.insert(2, "orange")
3. remove()	 : Removes the first occurrence of a value	my_list.remove("banana")
4. pop()	   : Removes an element by index and returns it	my_list.pop(1)
5. clear()	 : Removes all elements from the list	my_list.clear()
6. index()	 : Returns the index of the first occurrence	my_list.index("cherry")
7. count()	 : Counts the occurrences of a specific value	my_list.count("apple")
8. sort()	   : Sorts the list in ascending order	my_list.sort()
9. reverse() : Reverses the order of the list	my_list.reverse()
10. copy()	 : Returns a copy of the list	new_list = my_list.copy()

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# VIII. List Comprehension
 - It is a concise way to create lists in Python
 - A shortcut of for loop
 - It allows you to generate a new list by applying an expression to each item in an existing list

## Example 1: Create a list of squares 
my_input_list = [1, 2, 3, 4, 5]
### Using for loop
for value in my_input_list:
    my_output_list.append(value ** 2)
### Using list comprehension (shortcut of for loop)
my_output_list = [value**2 for value in my_input_list]


## Example 2: Create a list of squres of even numbers 
input_list = [1, 2, 3, 4, 5]
output_list = []
### Using for loop
for value in input_list:
    if value % 2 == 0:
        output_list.append(value ** 2)
### Using list comprehension (shortcut of for loop)
output_list = [value ** 2 for value in input_list if value % 2 == 0]

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# IX. List vs Tuple 
Feature	        List	         Tuple
Syntax	         []	            ()
Mutability	    Mutable	       Immutable
Performance	    Slower	       Faster
Usage	          Dynamic data	 Fixed data

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------























