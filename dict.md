# Index
1. What are dict ?
2. Key features
3. Defining & Accessing elements
4. Iterating
5. Dictonary methods
6. 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# I. What is dict ?
 -  Short for dictionary
 -  It is an unordered collection of key-value pairs
 -  A complex data type
 -  Mutable data type
 -  They allow fast lookups, additions, and updates
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# II. Key Features
 1. Key-Value pairs : so each key is associated with a value
 2. Keys must be immutable (e.g., strings, numbers, tuples) - but recommended strings
 3. Values can be of any data type
 4. Unordered : hence no concept of indexing, slicing
 5. Python dictionaries do not maintain order before Python 3.7.
    Note: Starting from Python 3.7, dictionaries preserve the insertion order as an implementation detail (guaranteed in Python 3.8+).
 6. Mutable data type - you can add, remove, or modify key-value pairs in a dictionary in-place
 7. Iterable type
 8. Hashing : Keys are hashed for quick lookups, making dictionary operations efficient
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# III. Defining & Accessing elements
 - Two ways :
    a. Using keys - RECOMMENDED
    b. Using get() method
   
customer_info = {
    "id": 1, 
    "firstName": "Venu",
    "lastName": "Koka",
    "age": 39,
    "isActive": True,    
}

print(type(customer_info))                                  # <class 'dict'>

print(customer_info["age"])                                 # Using Keys
print(customer_info.get("age"))                             # Using get() method (None if not found) - Avoids KeyError if the key does not exist
print(customer_info.get("email", "venu.koka@gmail.com"))    # Default value    

# IV. Iterating
Iterating Through a Dictionary
1. Loop Through Keys:
python
Copy code
for key in my_dict:
    print(key)
2. Loop Through Values:
python
Copy code
for value in my_dict.values():
    print(value)
3. Loop Through Key-Value Pairs:
python
Copy code
for key, value in my_dict.items():
    print(key, value)



Using dict() constructor:
python
Copy code
my_dict = dict(name='Alice', age=25, city='New York')
3. Using zip():
python
Copy code
keys = ['name', 'age', 'city']
values = ['Alice', 25, 'New York']
my_dict = dict(zip(keys, values))

Dictionary methods
Dictionary Methods
Method	Description
get(key[, default])	Returns the value for key, or default if the key is not found.
keys()	Returns a view object of the dictionary’s keys.
values()	Returns a view object of the dictionary’s values.
items()	Returns a view object of the dictionary’s key-value pairs.
update([other])	Updates the dictionary with the key-value pairs from another dictionary or iterable.
clear()	Removes all items from the dictionary.
copy()	Returns a shallow copy of the dictionary.
fromkeys(seq[, v])	Creates a new dictionary with keys from seq and values set to v.
setdefault(key[, v])	Returns the value for key if it exists; otherwise, inserts key with value v.
pop(key[, default])	Removes and returns the value for key, or default if key is not found.
popitem()	Removes and returns the last inserted key-value pair.
