# String

## Methods:

### Case
+ **Capitalize Case:** Capitalize the first character. `str.capitalize()`
+ **Casefold Case:** Return a casefold of the string. `str.casefold()`
+ **Lower Case:** Return a lower case of the string. `str.lower()`
+ **Title Case:** Capitalize all words's first character. `str.title()`
+ **Swap Case:** Invert the Case. `str.swapcase()`
+ **Upper Case:** Capitalize all chars. `str.upper()`
### Spacing
+ **Center:** Center a string, adding chars or white spaces. `center(width, [fillchar])`
+ **Determine tab size:** `str.expandtabs(tabsize=<int>)`
+ **Justify Left & Right:** `str.ljust(width, fillchar)`, `str.rjust(width, fillchar)`

### Validador
+ **Couting ocurrences:** `str.cout(sub, start, end)`
  + Returns a `int`.
+ **Suffix validador:** `str.endswith(suffix, start, end)`
  + Returns `bool`
+ **Finding an ocurrence:** `str**.find(sub, start, end)`
  + Returns a `bool`
  + `str.rfind()` gives the highest index.
  + [See Index - Returns a int](#validador)
+ **Finding an ocurrence index:** `str.index(sub, start, end)`
  + Returns a `int`
  + [See Find - Returns a bool](#validador)
+ **Is anything methods:** Always returns a `bool`
  + `str.isalnum()`: returns True to a alphanumeric.
  + `str.isalpha()`: returns True to a alphabetic.
  + `str.isdecimal()`: returns True to a decimal.
  + `str.isdigit()`: returns True to a digit.
  + `str.isnumeric()`: returns True to a number.
  + `str.isascii()`: returns True to a ASCII string.
  + `str.islower()`: returns True if the string have all chars lowed.
  + `str.isspace()`: returns True if have only white spaces.
  + `str.istitle()`: returns True to a TitleCase.
  + `str.isupper()`: returns True if the string have all chars upped.
+ + **Prefix validador:** `str.startswith(prefix, start, end)`
  + Returns `bool`



### Removing
+ **Strip Left & Right:** `str.lstrip([chars])`, `str.rstrip([chars])`
+ **Remove Prefix & Suffix:** `str.removeprefix(prefix, /)`, `str.removesuffix(suffix, /)`
+ **Replace:** `str.replace(old, new[, count])`
+ 


### Spliting
+ **Concatenating string:** `str.join(iterable)`.
  + The string will be a separator of the list in `join()`
  + ```py
    >>> test = {'2', '1', '3'}
    >>> s = ', '
    >>> print(s.join(test))
    >>> 2, 3, 1

    >>> test = {'Python', 'Java', 'Ruby'}
    >>> s = '->->'
    >>> print(s.join(test))
    >>> Python->->Ruby->->Java
    ```
+ **Split:** splits a string, based in sep occurrence `str.split(sep=string, maxsplit=-1)`
+ **Split Lines:** `str.splitlines()` the same as `str.split("\n")`

### Special
+ **Encode:** `str.encode(encoding="", errors="")`
  + Defaut encode = "uft-8"
  + errors can be: `ignore`, `strict`, `xmlcharrefreplace`, `backslashreplace`
+ **Inserting a string into another** `str.format(*args, **kwargs)`
  + [See More]()

[Read complete](https://docs.python.org/3/library/stdtypes.html#string-methods)

## String
---
### Immutability Principle
String are immutables, and you can't change it.

Look:
```py
>>> w = "word"
>>> w[0] = 'l'
...error text omitted...
TypeError: 'str' object does not support item assignment
```

But, you can do:
```py
>>> w = "word"
>>> w = "l" + w[:1]
```

It'll catch the "ord" and add the "l" in the start.

or:
```py
>>> w = "word"
>>> w = w.removeprefix("w")
```

or:
```py
>>> w = "word"
>>> w = w.replace("w", "l")
```
[Return](../Object%20Types.md#--strings)

---

### Working with quotes
+ An issue that happen in python with string operations are the quotes.

If you are using a double quote to delimit the string, you can use a single quote inside the string, but not a double quote. If you are using a single quote do delimit, you'll have the same problems, use the `\'` or just a `"`, but not a `'` into the string. 

```py
>>> print("don't")
don't
>>> print(""Hello, world" - C")
SyntaxError: invalid syntax

>>> print('don't')
SyntaxError: invalid syntax
>>> print('"Hello, world" - C')
"Hello, world" - C
```

To get around this problem, use a `\` before the quote to say that the `"` is into string:
```py
>>> print("\"Hello, world\" - C")
"Hello, world" - C
``` 
[Return](../Object%20Types.md#--strings)

---

### Triple Quotes `"""..."""`
+ These are used to set a string or a comment.
+ It can help you to write a multiple line string or a multiple line comment.
+ For break line in a string, just use `\` instead of `\n`, and go to another line. If you want write two lines in one line, use the \n.

Look:
```py
hello = """ Hello, everyone\
Welcome to my code!
"""

text = """Lorem,\
Ipaum\n is simply dummy text of the printing and typesetting industry.
"""

def function():
    """ Function is a function
    It's to explain the comentary after the structure `def func():`
    """
    pass
```
+ Triple quotes can be used explain a function
+ The first line define the title, and the second line, the explanation

<img src="../Assets/triplequotes_to_explain_function.png" alt="Triple quotes can be used explain a function" width="400px">

[Return](../Object%20Types.md#--strings)

---

### Concatenate Issue
+ On python you can concatenate a string with another without a add sign - `+`, but you can't concatenate a string with a variable this way.
```py
>>> 'Py' 'thon'
'Python'

>>> prefix = "Py"
>>> prefix 'thon'
  File "<stdin>", line 1
    prefix 'thon'
                ^
SyntaxError: invalid syntax


>>> prefix + 'thon'
'Python'
```
[Return](../Object%20Types.md#--strings)

---

### Selecting characteres by index

+ You can choose letters according to your index
+ The `[arg:arg]` after the variable do the choose
+ `[i]` select the letter on the address;
+ `[:i]` select all before the index `i`, that is, before the `i+1` letter.
+ `[i:]` select all from the index `i`, thst is, from the `i+1` letter.
+ `[i:n]` select all from `i` index that is before `n` index.
+ `[-i]` select the number by a inverse index. `i = -1` is the same as the last letter.
```py
>>> word = "Python"
>>> word[:2]
'Py'
>>> word[2:]
'thon'
>>> word[0]
'P'
>>> word[0:2]
'Py'
>>> word[2:5] 
'tho'
>>> word[-1]
'n'
```
+ Look the explanation from [Python.org](https://docs.python.org/3/tutorial/introduction.html#strings):
```
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1
```
[Return](../Object%20Types.md#--strings)

---
## Path
---
### Working with directories path
+ To determine a path, use the `r` before the path string. It'll avoid to have error with special commands, like `\n` or `\t`.
```py
>>> print('C:\Users\nicholas')
C:\Users

>>> print(r'C:\Users\nicholas')
C:\Users\nicholas
```
[Return](../Object%20Types.md#--strings)

---

## Read More
[Printf]()

