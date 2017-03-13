#HSLIDE
<img src="http://www.cakex.org/sites/default/files/National_Conservation_Training_Center.gif" width="200">
<img src="https://www.python.org/static/img/python-logo.png" width="400">
#### Python for Advanced GIS
<br>
<span style="color:gray">NCTC Advanced GIS</span>
<br>
<span style="color:gray">Daryl Van Dyke</span>

#HSLIDE
## Major Language Elements
* Hello, World!
* Variables and Types
* Lists
* Basic Operators
* String Formatting
* Basic String Operations
* Dictionaries, Sets, and Iterables
* Modules and Reusable code

#HSLIDE
## What is Python?

https://i.imgur.com/iymgGZV.jpg>

#HSLIDE
## What is Python?
* Interpreted language (JIT compilation)
* Uses the virtual machine model
The basic idea is that we have a python *process*, which sits and waits for instructions/compiled binary code (aka a virtual machine).

#HSLIDE
## Interpreter: Real Time vs. scripting
A huge benefit of python is that it is both an interface (shell) and program interpreter.
```python
>>>
```
This is the prompt.  It means we are running code in an interpreter, instead of running a script.
```python
>>> 1 + 1
2
>>> m = 1
>>> m + 1
```
#HSLIDE
## What is Python?

HelloWorld.py
```python
print "Hello World!"
print "Hello Again"
print "I like typing this."
print "I'd much rather you 'not'."
print 'I "said" do not touch this.'
```

#HSLIDE
## Flow Control - a basic code block
- Flow control is handled by 'blocks'.
- In Python, blocks are semantically derived from indents.
- The standard is 4 spaces.

#HSLIDE
## Flow Control - a basic code block
In other words, the units of program - the chunks of execution - all have the same indent level.

#HSLIDE
## A Simple Program
```python
#!/usr/bin/python
# That was a shebang (or hashbang) - it tells a \*nix system
#  what program to use to run the script.
#  Windows will ignore it.
#  This is a comment.  Use them, alot.
#  Tell yourself what you are doing, and why
#  They *must* have a hash sign in column 1.
def helloWorld():
     #  comments make other programmers take you seriously
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."

helloWorld()
```

#HSLIDE
## A Simple Program
```python
#  This is a function.  We'll look at them more closely...
#  but notice how the function definition _ends_ with the
#  move back to the 1st Column.  This ends the function
#  block.
def helloWorld():
     #  this function prints stuff
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."

helloWorld()
```

#HSLIDE
## A Simple Program
```python
def helloWorld():
     #  this function prints stuff
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."
#  with the function defined, we can call it.
helloWorld()
#   Because the function needs no inputs, we don't hand it any.
#   We can see this in both the declaration and the call.
```

#HSLIDE
## A Simple Program
```python
#!/usr/bin/python
def helloWorld():
    """
    This is a docstring.  They all have three
    quotes at beginning and end.  They show up magically
    in in-line help (the text that pops up.)
    """
     #  comments make other programmers take you seriously
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."

helloWorld()
```
#HSLIDE
## A Simple Program
```python
#!/usr/bin/python
def helloWorld():
    """ Function helloWorld()
    inputs:   <>
    returns:  <>   """
     #  dood, refactor this later for realz.  2016/01/30
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."
#  The function block ends by closing out of the indent (4 spaces).
#  That makes this the first line of code that actually does something
#      active, other than just define the function object in the compiler.
helloWorld()
```
#HSLIDE
### What is evaluation?
1. Interpreter starts reading through the program.
2. Interpreter sees the `def` keyword - this means that the next line will standardize indent size for this code block.
3. So it keeps reading until it gets to the bottom of the code block (indents back).
4. At that point, it compiles an object (everything is an object) that is a function.

#HSLIDE
### What is evaluation?
5. It then continues along until it gets to the call to that function, on the first column.
6. The call matches the object name, so any arguments in the parenthesis are passed to the object.
7. The function is evaluated with the input data, if any.

#HSLIDE
### What is evaluation?
8. Anything returned by the function (with the `return` keyword) is handed back to the calling block.
9. If there is an assignement, e.g.
`output = thisFunction(input)`,
 the LHS variable is mapped to the object in memory.
10. Otherwise, if there is no assignement, anything returned goes to standard out.

#HSLIDE
## What is Python?

HelloWorld_v1.py
```python
#!/usr/bin/python
# Let's do a better version
def helloWorld(inputText):
     #  comments make other programmers take you seriously
     print "Hello World!"
     print "Hello Again"
     print "I like typing this."
     print inputText
     return "I printed "+inputText+" just like you asked!"
#  so what happens with these?
helloWorld()
output = helloWorld("you do you...")
output = helloWorld(1+1)  # equivalent to helloWorld(1L+1L)
```
#HSLIDE
##

#HSLIDE
## Lists and Iterators
Lists are one of the most common data structures in Python.
* Compound data type
* make on with square brackets ```listNum = [1,2,3]``` or empty ```listE = []```
* lists are **mutable**

#HSLIDE
## List Indexing
Call it by it's position, 0-index.
```python
>>> listE = ["abba", 3, False]
>>> listE[0]
'abba'
>>> listE[-1]
False
>>> listE[0:1]
['abba']
>>> listE[0:2]
['abba', 3]
>>>
```
#HSLIDE
## List Indexing and Mutability
```
>>> listE[0] = "Iron Maiden"
>>> listE
['Iron Maiden', 3]
>>>
```
#HSLIDE
## `list` has some awesome methods!
Remember, any list is an instance of the List class.
Learning Python is a process of collecting memories of all these methods, and connecting them to problems.
##  Check the Docs alot!

#HSLIDE
## Commonly Used Methods
```python
>>> listE.append("this String")
>>> listE
['Iron Maiden', 3, False, 'this String']
>>> len(listE)
4
>>> #Nested list
>>> listF = ["Oh NO!", "This is too much!", True]
>>> listE.append(listF)
>>> listE
['Iron Maiden', 3, False, 'this String', ['Oh NO!', 'This is too much!', True]]
>>>
```
#HSLIDE
## More common ```list``` methods and functions
```python
>>> #Appended list
>>> listF = ["Oh NO!", "This is too much!", True]
>>> listEF = listE + ListF
>>> listEF
['Iron Maiden', 3, False, 'this String', 'Oh NO!', 'This is too much!', True
>>>
```
#HSLIDE
## Statements
### Assignment `=`
We recall:
1.  All python things are objects.
2.  All objects have classes - that is, **they are an instance of a class.**
  + Python has two fundamental flavors of objects.  Mutable and immutable.


#HSLIDE
## Statements
### Assignment `=`
Mutable Objects:
  + Mutable objects can be changed in place, immutable cannot.
  + When we 'change' immutable objects, we are really re-building that object and transferring the symbol name to that object.

#HSLIDE
## Assignment
<img src="https://i.stack.imgur.com/M3iZD.png">

#HSLIDE
##  Assignment
3. Assignment (token `=`, the equals sign).
  + Different than other C-style languages (C, Java, C++, etc).
  + Assignment in C, e.g., `x = 2`, translates to "typed variable name x receives a copy of numeric value 2".  

#HSLIDE
## Assignemnt: A Subtlety - C/Java vs. Python
1. The memory for this element (determined by data type and width) is allocated,
2. the data are copied over,
3. and the *variable name* is an alias or symbolic address for that memory location.  
4. Therefore, pointers, addresses, referencing, de-referencing, and pointer arithmetic.

#HSLIDE
## Statements
### Assignment *=* ... in Python
- ```x = 2``` - *in Python* - means:
"(generic) name x receives a reference to a separate, dynamically allocated object of numeric (int) type of value 2."
<img src="http://archive.oreilly.com/oreillyschool/courses/Python1/images/lessons/ModuleVsObjectSpace.jpg">
***This is termed binding the name to the object.***

#HSLIDE
### Assignment
 To be technical - they aren't variables.  They are names bound to objects.

 Names may be subsequently rebound at any time to objects of greatly varying types...
 -strings,
 -procedures,
 -complex objects with data and methods, etc.

#HSLIDE
### Assignment
OK - what happens?

`x = 2; y = 2; z = 2`

#HSLIDE
### Assignment
`x = 2; y = 2; z = 2`
three names and one numeric object,
to which all three names are bound.

#HSLIDE
### Assignement
Since a name is a generic reference holder it is unreasonable to associate a fixed data type with it.
However at a given time a name will be bound to some object, which will have a type;
***thus there is dynamic typing.***

#HSLIDE
### Assignment
Since it is just a name, pick a good one.  While you can do all of the above, why not?
Well, there are very good (and very advanced) reasons to do this... object polymorphism, for one.
Class inheritance and class hierarchies, another.
