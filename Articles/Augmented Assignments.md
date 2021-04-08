# Augmented Assignments

## Semantics

### Structure:
+ How to use:
  + `<x> <operator>= <y>`
+ How it runs:
  + `<x> = <x> <operator> <y>`

### Example:
```py
>>> # They are the same
>>> x += y
>>> x = x + y

>>> # Look:
>>> # Defining x and y
>>> x = 1
>>> y = 2
>>> x = x + y
>>> # 3 = 1 + 2
>>> x
3
>>> y
2
>>> x = 1
>>> x += y
>>> # 3 = (1) + 2
>>> x
3
```


## Operators:
+ `+=` 
+ `-=` 
+ `*=` 
+ `/=` 
+ `%=` 
+ `**=` 
+ `<<=` 
+ `>>=` 
+ `&=` 
+ `^=` 
+ `|=`
