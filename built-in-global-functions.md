# Built-in global functions
 - Python provides a set of built-in global functions that are always available for use.
 - These functions simplify a wide range of tasks 

## 1. Type Conversion Functions
int(x, base=10): Converts x to an integer.
float(x): Converts x to a floating-point number.
str(x): Converts x to a string.
bool(x): Converts x to a boolean.
list(iterable): Converts an iterable to a list.
tuple(iterable): Converts an iterable to a tuple.
set(iterable): Converts an iterable to a set.
dict(**kwargs): Creates a dictionary.
complex(real, imag): Creates a complex number.
bytes(source, encoding, errors): Creates a bytes object.
chr(i): Converts an integer to a Unicode character.
ord(c): Converts a Unicode character to its integer representation.

## 2. Mathematical and Logical Functions
abs(x): Returns the absolute value of x.
pow(x, y[, z]): Computes x raised to the power y (modulo z if provided).
round(number[, ndigits]): Rounds a number to ndigits precision.
divmod(x, y): Returns a tuple (quotient, remainder).
min(iterable, *args): Returns the smallest value.
max(iterable, *args): Returns the largest value.
sum(iterable, start=0): Returns the sum of an iterable.

## 3. Input/Output Functions
print(*objects, sep=' ', end='\n', file=sys.stdout): Prints objects to the console.
input(prompt): Reads input from the user.

## 4. Iterable and Sequence Manipulation
len(s): Returns the length of an object.
enumerate(iterable, start=0): Returns an enumerate object.
zip(*iterables): Combines iterables element-wise.
map(function, iterable): Applies a function to every item of an iterable.
filter(function, iterable): Filters items in an iterable.
reversed(seq): Returns a reversed iterator.
sorted(iterable, key=None, reverse=False): Returns a sorted list.

## 5. Object and Type Inspection
type(object): Returns the type of an object.
isinstance(object, classinfo): Checks if an object is an instance of a class.
issubclass(class, classinfo): Checks if a class is a subclass of another class.
id(object): Returns the memory address of an object.
dir([object]): Lists attributes and methods of an object
vars([object]): Returns __dict__ attribute of an object.
help([object]): Displays documentation for an object.

## 6. File and Directory Handling
open(file, mode='r', encoding=None): Opens a file.
eval(expression): Evaluates a Python expression.
exec(object): Executes Python code dynamically.

## 7. Miscellaneous
any(iterable): Returns True if any element is truthy.
all(iterable): Returns True if all elements are truthy.
bin(x): Converts an integer to a binary string.
hex(x): Converts an integer to a hexadecimal string.
oct(x): Converts an integer to an octal string.
hash(object): Returns the hash value of an object.
callable(object): Checks if an object is callable.
super([type[, object-or-type]]): Returns a proxy object for delegation.
