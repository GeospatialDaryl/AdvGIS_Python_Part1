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
- Hello, World!
- Variables and Types
- Lists
- Basic Operators
- String Formatting
- Basic String Operations
- Dictionaries, Sets, and Iterables
- Modules and Reusable code

#HSLIDE
## What is Python?

* Interpreted language (JIT compilation)
* Uses the virtual machine model
The basic idea is that we have a python *process*, which sits and waits for instructions/compiled binary code (aka a virtual machine).

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
9. If there is an assignement, e.g. `output = thisFunction(input)`, the LHS variable is mapped to the object in memory.
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
