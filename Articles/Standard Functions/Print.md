# Print Function and System Standard Output

## Python 2.6:

If you are using Python 2.6, the print expression doesn't need `()`.

And, it has three ways to print:
```py
# priting A and B
print A, B

# priting A and B with white space in end
print A, B,

# Priting A, B, C into a file
print >> _file, A, B, C
``` 
[See the equivalent in Python 3](#the-equivalent-to-python-2)

## Python 3:

### The equivalent to [Python 2](#python-26)
```py
# priting A and B
print(A,B)

# priting A and B with white space in end
print(A, B, end=" ")

# Priting A, B, C into a file
print(A, B, file=_file)
```
## Into Python Terminal
```py
>>> string = 'A'
>>> string
'A'

>>> integer = 10
>>> integer
10
```

## Using Sys
### Importing:
```py
import sys
```
### Printing:
```py
sys.stdout.write("Hello Python\n")
```


## Printing into files
+ Using Sys.Stdout:
```py
sys.stdout = open("file.ext", "a")
print(x, y, z)
```

+ Using Print Function:
```py
_file = open("file.ext", "a")
print(x, y, file=_file)
```

+ CSV Trick:
```py
>>> name, year, at = "Rick", 18, "@Github"
>>> print(name, year, at, sep=";", end="\n", file=open("file.csv", "a"))
>>> ### >> It'll print: "Rick;18;@Github\n" on csv
>>> ## Reading:
>>> print(open("file_example.txt").read())
Rick;18;@Github
```

+ Mixing:
```py
>>> # First, import the sys
>>> import sys

>>> # Define a variable as standard sys output
>>> temp = sys.stdout

>>> # Define the sys output a file instead of the terminal
>>> sys.stdout = open("file_example.txt", "a")

>>> # Print
>>> print(string_added_to_file)

>>> # Close the output
>>> sys.stdout.close()
>>> # Restore the output to standard
>>> sys.stdout = temp

>>> print(open("file_example.txt").read())
```


## Diference between `print()` and `sys.stdout.write()`:
### Using sys imported
+ You must to use `\n` in the end to break line.
+ You can't concatenate itens using `,`, you must to use `+`.
+ If you want add a write space, must to add `+ " " +`.
### Using defaut print function
+ You can use `,` and `+` to concatenate itens.
  + `,`: Concatenates the itens, and adds a write space between that.
  + `+`: Concatenates the itens without adds write space.



