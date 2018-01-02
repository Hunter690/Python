# Python

### General
“””: three quotation marks used before and after multiple line comment  
two shift8: exponent  
%: modulo, remainder  

### Strings

\: fix a string, placed before an apostrophe to stop a string from ending
[index]: placed after to denote the specific character in the string
	[index1:index2] returns everything from the letter at index 1 till right before the second index
len(): tells how many characters there are
.lower(): makes a string completely lower case
.upper(): makes a string completely upper case
str(): makes anything a string
%s % (string_1, string_2): % operator replaces a %s in a string with the string variable that comes after
print “string”, variable + number
string.split(): takes a string a makes into a list
float(): make into decimal number
Comparators: check if a value is (or is not) equal to, greater than (or equal to), or less than (or equal to) another value
==: equal to
!=: not equal to
<=: less than or equal to
>=: greater than or equal to
not: gives the opposite of the statement
	Not True is False
Boolean operations:
	1. not is evaluated
	2. and is evaluated
	3. or is evaluated
Conditional Statement
if some_function():
    # block line one
    # block line two
    # et cetera
There should never be anything in following else
raw_input(): accepts a string, prints it, and waits for user response
.isalpha(): returns true when there are only characters
Function: 
	1. header: def, name of function, parameters, and colon
	2. body: describes the procedures the function carries out
Call a function by typing the name of the function and parameters (if it has any)
Parameter: acts as a variable name for an argument
ANONYMOUS FUNCTION
lambda x: x % 3 == 0
	does the same thing as def by_three(x):
    					return x % 3 == 0
	with lambda, you don’t have to name the function which makes it anonymous
filter: filters out stuff
Lists
lists: datatype used to store information as a sequence under a single variable name
	assign items to a list: list_name = [item_1, item_2]
list_name[index]: tells what is there
.append(): adds to a list; only takes one argument
.index(): tells the first index of the argument; works with strings
.insert(index, string): inserts the string at the index and moves everything down 1 index
sorted(list): sorts everything in order
.sort(): sorts everything in a list into alphabetical order (or numerical order)
.remove(item): removes item from list
list.pop(index) will remove the item at index from the list and return it to you
del(list[1]) is like .pop in that it will remove the item at the given index, but it won't return it
.join(list_name): joins the things in the list together by whatever comes before the .join
	Ex. letters = ['a', 'b', 'c', 'd']
print " ".join(letters)
#prints out: a b c d
LIST COMPREHENSION
new_list = [x for x in range(1,6)]
# => [2, 4, 6, 8, 10]
LIST SLICING
[start:end:stride]
	When using the default start/end, still need to use colon
	A negative stride goes from right to left
For Loops
for variable in list_name:

Dictionaries
d = {'key1' : 1, 'key2' : 2, 'key3' : 3}

Dictionary called d with three keys, ‘key1’ has a value of 1 and so on
	refer to thing before colon to get value after colon
	only accepts one argument
dict_name[new_key] = new_value
adds a dictionary entry
del dict_name[key_name]
removes a dictionary entry
dict_name[key] = new_value
assigns a new value to a key
you can go to any key by typing: dict_name[key]
dictionary_name.keys(): returns dictionary keys
dictionary_name.values(): returns dictionary values
Range:
range(6) # => [0,1,2,3,4,5]
range(1,6) # => [1,2,3,4,5]
range(1,6,3) # => [1,4]

range(stop)
range(start, stop)
range(start, stop, step): step is how much each item increases by
Loops
while: similar to if statement; executes code inside of it if some condition is true
else block will execute anytime the loop condition is evaluated to False
	in the case of a break, else will not be executed
enumerate function: supplies index to each element in a list that is passed in a loop
	for variable in enumerate(list)
zip: passes two (or more) lists, creating pairs (or larger) at the list index; stops at the shorter list
	for variable, another_variable in zip(list_a, list_b):
break ends a for loop
File I/O:
editing a file:
my_file.write("Data to be written")
write(): takes string argument 
	in order to write values on separate lines: file_name.write(“string” + “\n”)
file_name.read(): reads the file
	.readline(): each time .readline() is called, the next line will be returned/printed
OPENING AND CLOSING FILES:
with open("file", "mode") as variable:
    # Read or write to the file
open(“text_file”, “letter”): opens the text file in a certain mode (w stands for write, r stands for write, r+ stands for read and write)
my_file.close(): closes a file; always needs to be done
file_name.closed: if the file is closed, it returns true; otherwise, it returns false
Class: 
objects: data structure that contains data and function
method: functions of objects
class: way of organizing and making objects with similar characteristics and functions
pass: does nothing, allows something to function without having to have something
class NewClass(object):
	class keyword, name of class, and new class; user defined class name starts with Letter
__init__(): function that initializes the objects created; usually use self as the parameter in init
	gets called whenever a new instance of a class is created; exists by default, but defining the function overrides the default
dot notation: puts attributes to objects; can access attribute by variable_name_of class.attribute_name
	Used to tell an instance of a class to use a method (function) in that class
	instance.method() calls the method written in class because the instance is an instance of the class
	Ex of classes: Integers, Floats, Strings, Lists, Dictionaries, and Booleans
		Ex of methods: Inside the List class, .append() is a method
	assigns a variable to a class, creating a member variable
self: self is the first parameter in __init(); Python uses the first parameter of __init__() to refer to the object being created; gives the object created its identity
inheritance: in the case where there is an is-a relationship (e.g. panda is a bear) the specific class could inherit from the more general class
	class DerivedClass(BaseClass):
super: if you override a class that has a function you still need
class Derived(Base):
   def m(self):
       return super(Derived, self).m(arguments_the_method_takes)
	m would be the method from the base class that you need
__repr__(): “representation”; built-in method that overrides; 
Etc.
The , character after our print statement means that our next print statement keeps printing on the same line
module: file that contains definitions (variables and functions) that someone can use once it is imported
	when using a function from a module, you have to type module_name.function_name
generic import: imports everything from a module
function import: pulls in a single function form a module using from
	general formula: from module import function
universal import: import all variables and functions in a module without having to type module_name.
	general formula: from module import *
max(): takes any number of arguments and returns the largest one
min(): returns the smallest of arguments
abs(): returns absolute value of argument
type(): returns type of data of argument
int(): returns an integer
	int(string, base): converts the number into base 10 from the base
Bitwise Operators
0b: start a binary number and python can interpret it
bin(): takes an integer and returns it in binary
BIT SHIFT
0b000001 << 2  # 0b000100 (1 << 2 = 4)
0b0010100 >> 3 # 0b000010 (20 >> 3 = 2)
integer & another_integer: compares the two numbers at a bit level and returns all the similarities
	a:   00101010   42
     	b:   00001111   15       
===================
    a & b:   00001010   10
integer | another_integer: similar to and, if either exhibits it, it returns
	a:  00101010  42
    	b:  00001111  15       
================
    a | b:  00101111  47
integer ^ integer: like the |; if either of the corresponding bits of the two numbers are on, but not both
	a:  00101010   42
    	b:  00001111   15       
================
     a ^ b:  00100101   37

~integer: flips all the bits (adds one and multiplies by negative 1)
mask = some_bit: set a variable called mask; check to see if a bit is turned on by running it through an if statement:
	num  = 0b1100
	mask = 0b0100
	desired = num & mask
	if desired > 0:
    		print "Bit was on"

	can also turn a mask on using |
	can also switch everything to opposite setting by using mask = 0b1111111… and ^
