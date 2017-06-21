# Bitwise OR (|)

The bitwise OR operator in C++ is the vertical bar symbol, |. Like the & operator, | operates independently each bit in its two surrounding integer expressions, but what it does is different (of course). The bitwise OR of two bits is 1 if either or both of the input bits is 1, otherwise it is 0. In other words:
```C++
    0  0  1  1    operand1
    0  1  0  1    operand2
    ----------
    0  1  1  1    (operand1 | operand2) - returned result
```
Here is an example of the bitwise OR used in a snippet of C++ code:
```C++
    int a =  92;    // in binary: 0000000001011100
    int b = 101;    // in binary: 0000000001100101
    int c = a | b;  // result:    0000000001111101, or 125 in decimal.
```
Example Program for Arduino Uno

A common job for the bitwise AND and OR operators is what programmers call Read-Modify-Write on a port. On microcontrollers, a port is an 8 bit number that represents something about the condition of the pins. Writing to a port controls all of the pins at once.

PORTD is a built-in constant that refers to the output states of digital pins 0,1,2,3,4,5,6,7. If there is 1 in an bit position, then that pin is HIGH. (The pins already need to be set to outputs with the pinMode() command.) So if we write PORTD = B00110001; we have made pins 0,4 & 5 HIGH. One slight hitch here is that we may also have changeed the state of Pins 0 & 1, which are used by the Arduino for serial communications so we may have interfered with serial communication.
```C++
*Our algorithm for the program is:*
```
* Get PORTD and clear out only the bits corresponding to the pins we wish to control (with bitwise AND).
* Combine the modified PORTD value with the new value for the pins under control (with biwise OR). C++

```
int i;     // counter variable
int j;

void setup(){
DDRD = DDRD | B11111100; // set direction bits for pins 2 to 7, leave 0 and 1 untouched (xx | 00 == xx)
// same as pinMode(pin, OUTPUT) for pins 2 to 7
Serial.begin(9600);
}

void loop(){
for (i=0; i<64; i++){

PORTD = PORTD & B00000011;  // clear out bits 2 - 7, leave pins 0 and 1 untouched (xx & 11 == xx)
j = (i << 2);               // shift variable up to pins 2 - 7 - to avoid pins 0 and 1
PORTD = PORTD | j;          // combine the port information with the new information for LED pins
Serial.println(PORTD, BIN); // debug to show masking
delay(100);
   }
}
```

