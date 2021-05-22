# Python Cheatsheet
Cheatsheets are good when you want to revise some of the concepts, but a idle way to start learning <br/>
I would recommend you to learn in depth from this course: [Udemy Course](https://www.udemy.com/course/complete-python-bootcamp/)
<br/>If you can self learn Repository: [Github](https://github.com/Pierian-Data/Complete-Python-3-Bootcamp)

## Theory
- Python is a scripting language.
- **Scripting vs Compiled ?** - Language like c++/java's code needs to compiled by its compiler, after compilation it is just machine level code.
Where as in a scripting language its interpreter will be run the code one the spot one line at a time.

## VSCODE extension:
- Python
- Python for vscode
- Magic Python
- Arepl

## Making a virtual env: 

### **Why Virtual env?**
Because managing python dependencies is a mess, this will install dependencies for that project only instead of globally.

- `python -m venv venv` this will create a venv folder in your directory.
- `source ./venv/bin/activate` this will activate this virtual env.
 
## Comments in python
- single line use `#`
```python
# single line comments
```
- multiline use `'''`. often called as docstring, as it is just to document function/classes. 
```python
'''
This is a example of 
Multiline comment.
'''
```

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

## Naming conventions:
- Use underscore for variables.
- variables cannot Start with a number.
- Avoid special meaning keywords.
- Use snake case for functions.
- Use CamelCase for Classes names.

## Printing in Python:
```python
print("")
```

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
 ---
Hello
world\
Yeahh!!
"Quotes"
'Single quote'
 ---
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

## Sets in Python
Sets are an unordered collection of unique elements. 
```python
a = set()
a.add(1)
a.add(1)
a.add(1)
print(a) # {1}
```
### Convert list to set
```python
a = [1,1,2,2,2,3,3,3]
a = set(a)
``` 

## File IO with Python
### init file obj
```python
file = open("file.txt")
```
### read contents
```python
contents = file.read()
print(contents)
```
### move the cursor/pointer
```python
file.seek(0)
```
### read line by line
```python
contents = file.readlines() # returns list of lines.
```
### close the file
```python
file.close()
```
### Using context manager
```python
with open("file.txt") as file:
    print(file.read())
```
### different modes for file
- `r`: Read
- `r+`: Read and Write
- `w`: Write (will override the file)
- `w+`: Write + Read (will override the file)
- `a`: Append the file

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

## Python Statements:
Indentation is **important** in the python.
### if, elif, else
```python
loc = 'Bank'

if loc == 'Auto Shop':
    print('Welcome to the Auto Shop!')
elif loc == 'Bank':
    print('Welcome to the bank!')
else:
    print('Where are you?')
```
### for loops
```python
# iterate list/string/tuple
l = [1,2,3]
for item in l:
    print(item)
# extraction made easy
list2 = [(2,4),(6,8),(10,12)]
for t1,t2 in list2: # Same as dict. t1 will be key, t2 will be value.
    print(t1) # will print 2,6,10
# Protip about dict: use .value() and .keys() for looping Values/keys.
```
### white loops
in python we can use python with else statement.
```python
x = 1
while x < 3:
    print(f"x is {x}")
    x = x + 1
else:
    print("Uhhoo! x > 3")
```
### Statement in python
- **break**: Breaks out of the current closest enclosing loop.
- **continue**: Goes to the top of the closest enclosing loop.
- **pass**: Does nothing at all, Programmers use this for placeholder.
```python
def future_method():
    # Todo: implement it later.
    pass
while True:
    break
for i in range(10):
    if i == 5:
        #omit
        continue 
    print(i)
```
## Some useful operators 
### range()
range is a generator.
<br/> **Syntax**: `range(start,end,step)`
<br/> 
Use directly with loops for iteration.

```python
a = list(range(0,11,2)) # returns 0,2,4,..10
```
### enumerate()
with help of this we can keep track of index and value.
```python
a = [20,100,5,3,6]
for index,value in enumerate(a):
    print(f"{index}\t{value}")
```
### zip()
```python
zip multiple lists.
a = [1,2,3]
b = [4,5,6]
for item in zip(a,b):
    print(item)
```
### in operator:
```python
a = [1,2,3]
print(3 in a) # True
```
### min and max:
```python
a = [1,2,3]
print(min(a)) # 1
print(max(a)) # 3
```
 

## List Comprehensions
Quicker and unique way to create lists.
```python
# Grab every letter in string
lst = [x for x in 'word']

# Square numbers in range and turn into list
lst = [x**2 for x in range(0,11)]

# Check for even numbers in a range
lst = [x for x in range(11) if x % 2 == 0]
```

## help function in python
if you are lazy like me, want to learn documentation about specific inbuilt method via terminal, you can use help()
```python
a = [1,2,3]
help(a.insert) # will print info about this method
```

## Functions in python
### Basic function with argument and default value
```python
# def keyword to define functions.
def say_hello(name="world"):
    print(f"Hello {name}!")
    # or return f"Hello {name}!" if you want to return it.
```
### *args and **kwargs
- `*args`: N number of arguments, returns tuple.
- `**kwargs`: N number of keyword arguments, returns dict.
```python
def total_income(*args, **kwargs):
    print(f"Income for month, {kwargs['month']} is : {sum(args)}")
total_income(10,20,300,month="July")
```
### lamda, filter and map
```python
#map
def square(num):
    return num**2
my_nums = [1,2,3,4,5]
map(square,my_nums) # 1, 4, 9, 16, 25

# filter
def check_even(num):
    return num % 2 == 0
nums = [0,1,2,3,4,5,6,7,8,9,10]
filter(check_even, nums) # 0, 2, 4, 6, 8, 10

# lets convert each of the above function to lambda.
map(lambda num:num**2,my_nums)
filter(lambda num:num%2==0, nums) 
```
## Classes in python
### Basic implementation
```python
class Circle:
    pi = 3.14

    # Circle gets instantiated with a radius (default is 1)
    def __init__(self, radius=1):
        self.radius = radius 
        self.area = radius * radius * Circle.pi

    # Method for resetting Radius
    def setRadius(self, new_radius):
        self.radius = new_radius
        self.area = new_radius * new_radius * self.pi

    # Method for getting Circumference
    def getCircumference(self):
        return self.radius * self.pi * 2


c = Circle()

print('Radius is: ',c.radius)
print('Area is: ',c.area)
print('Circumference is: ',c.getCircumference())

```
### Inheritance
```python
class Animal:
    def __init__(self):
        print("Animal created")

    def whoAmI(self):
        print("Animal")

    def eat(self):
        print("Eating")


class Dog(Animal):
    def __init__(self):
        Animal.__init__(self)
        print("Dog created")

    def whoAmI(self):
        print("Dog")

    def bark(self):
        print("Woof!")
```
### Polymorphism
```python
class Animal:
    def __init__(self, name):    # Constructor of the class
        self.name = name

    def speak(self):              # Abstract method, defined by convention only
        raise NotImplementedError("Subclass must implement abstract method")


class Dog(Animal):
    
    def speak(self):
        return self.name+' says Woof!'
    
class Cat(Animal):

    def speak(self):
        return self.name+' says Meow!'
    
fido = Dog('Fido')
isis = Cat('Isis')

print(fido.speak())
print(isis.speak())
```
### Using Special methods
Just like `__init__` we have more special methods.
```python
class Book:
    def __init__(self, title, author, pages):
        print("A book is created")
        self.title = title
        self.author = author
        self.pages = pages

    def __str__(self):
        return "Title: %s, author: %s, pages: %s" %(self.title, self.author, self.pages)

    def __len__(self):
        return self.pages

    def __del__(self):
        print("A book is destroyed")


book = Book("Python Rocks!", "Jose Portilla", 159)

#Special Methods
print(book)
print(len(book))
del book
```

## Exception Handling
### try, except, finally, and else.
```python
def askint():
    while True:
        try:
            val = int(input("Please enter an integer: "))
        except:
            # You can also expect specific error like TypeError or generic type Exception
            print("Looks like you did not enter an integer!")
            continue
        else:
            print("Yep that's an integer!")
            break
        finally:
            print("Finally, I executed!")
        print(val)
```
