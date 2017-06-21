# continue

The continue statement skips the rest of the current iteration of a loop (**do**, **for**, or **while**). It continues by checking the conditional expression of the loop, and proceeding with any subsequent iterations.

## Example

```C++
for (x = 0; x < 255; x ++)
{
    if (x > 40 && x < 120){      // create jump in values
        continue;
    }

    analogWrite(PWMpin, x);
    delay(50);
}```