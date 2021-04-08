# Naming Variables

## Reserved Words:

Python has reserved words, that you can't use.
If you import a module, you must to care with the module's reserved words too.

### List:

|Python's |Reserved |Words    |
|:-------:|:-------:|:-------:|
|and      |False    |nonlocal |
|as       |finally  |not      |
|assert   |for      |or       |
|break    |from     |pass     | 
|class    |global   |raise    |
|continue |if       |return   |
|def      |import   |True     |
|del      |in       |try      |
|elif     |is       |while    |
|else     |lambda   |with     |
|except   |None     |yield    |

## Rules:

+ In Python you can use numbers in variables, but you can't start a variable name with a number, look:
```py
>>> 1name = "Linus"
SyntaxError: invalid syntax
>>> name1 = "Linus"
>>> name
'Linus'
``` 
+ But also, you can't use special characteres in you string, just use alphanumerics chars and the underline.
