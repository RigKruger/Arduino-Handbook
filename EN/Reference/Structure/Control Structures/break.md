# break

**break** is used to exit from a **do**, **for**, or **while** loop, bypassing the normal loop condition. It is also used to exit from a **switch** statement.

## Example
```C++
for (x = 0; x < 255; x ++)
{
    analogWrite(PWMpin, x);
    sens = analogRead(sensorPin);  
    if (sens > threshold){      // bail out on sensor detect
       x = 0;
       break;
    }  
    delay(50);
}```
