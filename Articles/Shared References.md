# Shared Reference Issue

## Different Objects
When no reference is made to First object, but to equal list, the Second object ins't the same as the First, but have the same value.
```py
>>> ListA = ['a', 'b', 'c']
>>> ListB = ['a', 'b', 'c']

>>> ListA == ListB
True

>>> ListA is ListB
False
```

## Same Objects
Already, when reference is made to First Object, the Second will be the same object.
```py
>>> ListA = ['a', 'b', 'c']
>>> ListB = ListA

>>> ListA == ListB
True

>>> ListA is ListB
True
```