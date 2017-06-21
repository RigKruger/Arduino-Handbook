# % (modulo)

## Description:

Calculates the remainder when one integer is divided by another. It is useful for keeping a variable within a particular range (e.g. the size of an array).

## Syntax:
```C++
result = dividend % divisor
```
## Parameters:

dividend: the number to be divided

divisor: the number to divide by

## Returns:

the remainder

## Examples:
```C++
x = 7 % 5;   // x now contains 2
x = 9 % 5;   // x now contains 4
x = 5 % 5;   // x now contains 0
x = 4 % 5;   // x now contains 4
```

## Example Code:
```C++
/* update one value in an array each time through a loop */

int values[10];
int i = 0;

void setup() {}

void loop()
{
  values[i] = analogRead(0);
  i = (i + 1) % 10;   // modulo operator rolls over variable  
}
```

## Tip

The modulo operator does not work on floats. 