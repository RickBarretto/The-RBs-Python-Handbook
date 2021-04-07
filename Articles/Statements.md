# Python Statements - Examples

## Create references - Assigment
```py
>>> a, *b = "a", "b", "c"

>>> print(a)
>>> 'a'
>>> print(b)
>>> ['b', 'c']
```

## Running expressions
```py
log.write()
print(args)
```

## Selecting actions - if/else/elif
```py
if i == 0: 
    print("zero")
elif i%2 == 0: 
    print("pair")
else: 
    print("odd")
```

## Sequence iteration/General loops - for/while
```py
for i in range(number): 
    print(i)
    while i < 10: 
        print("i < 10")
```

## Empty placeholder - pass
```py
def hello(): 
    pass
```

## Loop exit - break
```py
while i < 10: 
    i += 1
    if i == 5: 
        break
```

## Loop continue - continue
```py
for user in UserList:
    if user != "Steve":
        continue
    else:
        break
```

## Functions and methods - def
```py
def add(args):
    """ aaaaaaaaaaaaaaaaa
    bbbbbbbbbbbbbbb
    """
    sum_list = []
    for n in range(args):
        sum_list.append(n)
        print(sum(sum_list))
```

## Functions return - return
```py
def add(args): 
    sum_list = []
    for n in range(args): 
        sum_list.append(n)
        return sum(sum_list)
```

## Function generator - yeld
```py
def generator(args): for i in range(args): yield i*2
```

## Namespaces - global
```py
x = 'person_1'
def function(): 
    global x, y; x = 'person_2'
```

## Namespaces(3.0+) - nonlocal
```py
def function(): x  = 'person_1'
    def internal_function(): 
        nonlocal x; x = 'new'
```

## Module acess, Attribute and Local-Rename
```py
import math; from math import sqrt; import tensorboard_launcher as tl
```

## Building objects - class
```py
class Subclass(SuperClass): staticData = []
    def methods(self): pass
```

## Catching exceptions - try/except/finally
```py
try: action()
except: print("Error")
```

## Triggering exceptions - raise
```py
raise EndSearch(loc)
```

## Debugging checks - assert
```py
assert X > Y, "X too small"
```

## Context Managers - with/as
```py
with open("text.txt", "r") as myText:
    process(myText)
```

## Deleting references - del
```py
del data[k]
```