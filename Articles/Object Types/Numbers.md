# Numbers

## Operations
---
### Math Operations
+ Sum: `x + y`
+ Difference: `x - y`
+ Product: `x * y`
+ Quotient: `x / y`
+ Floored Quotient: `x // y`
+ Remainder: `x % y`
+ Invert Signal: `-x`
+ Power: `x ** y`

[Return](../Object%20Types.md#--numbers)

---
### Methods
+ Absolute value (always positive): `abs(x)`
+ Complex number: `complex(re, im)`
  + Example: `complex('1 + 2j') `
+ Conjugate of a complex number: `num.conjugate()`
+ Floored Quotient and Remainder: `divmod(x, y)`
  + Returns: `(x // y, x % y)`
+ Power: `pow(x, y)`
  + The same as `(x ** y)`

[Return](../Object%20Types.md#--numbers)

---
### Convert
+ Convert to integer: `int(x)`
+ Convert to float point: `float(x)`

[Return](../Object%20Types.md#--numbers)

---
## Float
---
### Float equals
+ The quation 3.5 + 2.0 isn't equal to 3.5.
+ Float operations aren't exact. This happens because the float isn't a decimal fration, but a binarie fration.

Look, the decimal **0.1** is actually **0.1000000000000000055511151231257827021181583404541015625**, weird, isn't it?

> Read more in: [Float Limitations](https://docs.python.org/3/tutorial/floatingpoint.html)

**Contorning the issue:** 
```py
>>> import math
>>> sum([0.1] * 10) == 1.0
False
>>> math.fsum([0.1] * 10) == 1.0
True
```
[Return](../Object%20Types.md#--numbers)

---

## Integer
---
### How many digits have a number?
+ For this, use: 
```py
>>> len(str(num))
```
> **Explanation:** we turn the number in a string, and we use the len( ) method to calculate the range.


[Return](../Object%20Types.md#--numbers)

---