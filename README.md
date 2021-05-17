# Python Cheatsheet
Cheatsheets are good when you want to revise some of the concepts, <br/>
I would recommend you to learn in depth from this course: [Udemy Course]([https://link](https://www.udemy.com/course/complete-python-bootcamp/))
<br/>If you can self learn Repository: [Github](https://github.com/Pierian-Data/Complete-Python-3-Bootcamp)

----------

## VSCODE extension:
- Python
- Python for vscode
- Magic Python
- Arepl

## Making a virtual env:
----------

### **Why Virtual env?**
Because managing python dependencies is a mess, this will install dependencies for that project only instead of globally.

- `python -m venv venv` this will create a venv folder in your directory.
- `source ./venv/bin/activate` this will activate this virtual env.
----------


## Data Types:
- int # Whole Numbers
- float # Number with decimals.
- str # String
- list # ordered sequence of object
- dict # unordered key-value pairs.
- tup # ordered immutable seq. of objects.
- set # Unordered collection of unique objs.
- bool # Logical value True / False.
- None # no value
----------

## Naming conventions:
- Use underscore for variables.
- variables cannot Start with a number.
- Avoid special meaning keywords.
----------

## Printing in Python:
```python
print("")
```
----------

## Numbers in Python:
```python
print(1+2) # Addition
print(3-2) # Subtraction
print(3*2) # Multiplication
print(3/2) # Division
print(3%2) # Mod.
print(3**2) # Power
print((3 + 10) * 15) # Using Braces.
```
## Using with variables:
```python
a = 10
print(a)
# TO check the type:
print(type(a))
```
### Variables makes it easy to understands the code.
```python
my_income = 100
tax_rate = 0.1
my_taxes = my_income*tax_rate
print("My income tax is",my_taxes)
```
----------

## Strings in Python:
String is nothing but ordered seq. of characters.
Note: Strings are immutable

### Using directly with print:
```python
print("Simple String")
print('Add quotes inside the  "string" by using single quote.')
print("concat string "+"like this")
```
### Taking Input
```python
greeting = "Hello"
name = input("Enter your name: ")
print(greeting + ' ' + name)
```
### Use `,` instead of `+` This will auto seprate them by spaces.
```python
print(greeting,name)
```
### Escape characters in python:
```python
print("Hello\nWorld")
# or
print("""
-------------
Hello
world\
Yeahh!!
"Quotes"
'Single quote'
-------------
""")
```
### Check the length of string:
```python
print(len("Hey"))
```
### String indexing
```python
a = "Hello"
a[0] Will return H
```
### String Slicing
```python
a[start:end:step]
a[0:2] # Start from 0th index till 2(excluding)
a[::2] # Step will be 2.
# We can use this to print a string backwards
s[::-1]
```
----------

### String methods:
```python
# Multiply Strings
a = 'H' * 10
```
```python
# Upper Case a string
s.upper()
```
```python
# Lower case
s.lower()
```
```python
# Splitting
s.split('W')
s.split() # split via whitespace.
```
### Formatting strings:
- `.format()`
- `f""` F-string
```python
print('The {2} {1} {0}'.format('fox','brown','quick'))
print('First Object: {a}, Second Object: {b}, Third Object: {c}'.format(a=1,b='Two',c=12.3))
num = 23.45
print("My 10 character, four decimal number is:{0:10.4f}".format(num))
print(f"My 10 character, four decimal number is:{num:10.4f}")
```
### String Print alignment
```python
left_alignment = "Left Text"
center_alignment = "Centered Text"
right_alignment = "Right Text"
print(f"{left_alignment : <20}|{center_alignment : ^15}|{right_alignment : >20}")
More about this: https://pyformat.info/
```
----------

## Lists in Python:
### Basic Usage
```python
# Supports dynamic types, as it is python :)
my_list = [100,2.5,"Mohit"]
# len(my_list) for length
# Change objs:
my_list[0]=1000
```
**Slicing is same as String slicing**
### Concat
```python
a = [1,2,3]
b = [4,5]
c = a + b
```
### Append the list
```python
my_list.append(10.8)
```
### Poping objs
```python
my_list.pop(index) # default index is -1, returns popped element.
```
### Sorting
```python
a = [1,2,3]
a.sort() # in-place sort, it will modify the list, returns None
# Tip: use sorted(a) it will return the value instead of in-place
```
### Reverse
```python
a = [1,2,3]
a.reverse() # also in-place
```
### Nested list
```python
a = [1, 2, 3, [4,5,]]
print(a[3][1]) # Returns 5.
```
----------

## Dictionaries in Python
Unordered key-value mappings, basically you can have custom keys
</br>Think it like, you can use this to make dynamic variables, where key will be the variable name.
</br>Like list value can be any data type.

### Basic Usage
```python
prices = {"apple":10, "orange":20.5}
print(prices)
print(prices["apple"])
print(prices.keys()) # get keys
print(prices.values()) # get values
print(prices.items()) # get items, return tuples with keys and values
print(prices.pop("apple")) # Pop the object
print(prices)
print(prices.clear()) # Clear All
print(prices)
print(prices.get("banana")) # it will check if it is present, return None if not.
print(prices.__contains__("apple")) # Returns true/false
```
----------

## Tuples in Python
Same as list, but immutable.
### Basic Usage
```python
a = (1,2,2,4)
print(a)
# Interesting Fact: tuple supports only two methods:
a.count(2) # This can be use with list as well.
a.index(3) # This can be use with list as well.
```
----------

# Sets in Python
Sets are an unordered collection of unique elements. 
```python
a = set()
a.add(1)
a.add(1)
a.add(1)
print(a) # {1}
```
# Convert list to set
```python
a = [1,1,2,2,2,3,3,3]
a = set(a)
```
----------

## File IO with Python
## init file obj
```python
file = open("file.txt")
```
## read contents
```python
contents = file.read()
print(contents)
```
## move the cursor/pointer
```python
file.seek(0)
```
## read line by line
```python
contents = file.readlines() # returns list of lines.
```
## close the file
```python
file.close()
```
## Using context manager
```python
with open("file.txt") as file:
    print(file.read())
```
## different modes for file
- `r`: Read
- `r+`: Read and Write
- `w`: Write (will override the file)
- `w+`: Write + Read (will override the file)
- `a`: Append the file

----------

## Chaining comparison operators:
To chain `==, != <, >, >=, <= and is` these operators, we have these logical operators
- and
- or
- not
```python
if 2 > 3 and 2 > 5:
    print("I am inevitable")
if "hello" is "world" or "india" is "country":
    print("Yeah!!")
if not 10 == 10:
    print("Tough luck!" )
```
