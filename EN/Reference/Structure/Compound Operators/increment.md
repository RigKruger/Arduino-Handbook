# ++ (increment) / -- (decrement)

## Description:

Increment or decrement a variable

## Syntax:
```C++
x++;  // increment x by one and returns the old value of x
++x;  // increment x by one and returns the new value of x

x-- ;   // decrement x by one and returns the old value of x 
--x ;   // decrement x by one and returns the new value of x  
```
## Parameters:

x: an integer or long (possibly unsigned)
Returns

The original or newly incremented / decremented value of the variable.
## Examples:
```C++
x = 2;
y = ++x;      // x now contains 3, y contains 3
y = x--;      // x contains 2 again, y still contains 3 
```