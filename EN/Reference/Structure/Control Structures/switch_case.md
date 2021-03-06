# switch / case statements

Like **if** statements, **switch...case** 
controls the flow of programs by allowing programmers to specify 
different code that should be executed in various conditions.  In 
particular, a switch statement compares the value of a variable to the 
values specified in case statements.  When a case statement is found 
whose value matches that of the variable, the code in that case 
statement is run.  

The **break** keyword exits the switch statement, and is
 typically used at the end of each case.  Without a break statement, the
 switch statement will continue executing the following expressions 
("falling-through") until a break, or the end of the switch statement is
 reached.

## Example
```C++
switch(var){  
    case1:  
      //do something when var equals 1  
      break;  
    case2:  
      //do something when var equals 2  
      break;  
    default:  
      // if nothing else matches, do the default  
      // default is optional  
    break;  
  }
```

## Note

Please note that in order to declare variables within a case brackets are needed. An example is showed below.
```C++
switch(var){  
    case1:  
      {  
      //do something when var equals 1  
      int a =0;  
      .......  
      .......  
      }  
      break;  
    default:  
      // if nothing else matches, do the default  
      // default is optional  
    break;  
  }
```
## Syntax
```C++
switch(var){  
  case label:  
    // statements  
    break;  
  case label:  
    // statements  
    break;  
  default:  
    // statements  
  break;  
}
```

## Parameters

var: the variable whose value to compare to the various cases

label: a value to compare the variable to