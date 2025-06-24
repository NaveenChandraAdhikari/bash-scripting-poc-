## IF statements

### format
```bash
if [ <some test> ]
then
<commands>
fi
```
***NOTE:Anything between then and fi (if backwards) will be executed only if the test (between the square brackets) is true**


- EXAMPLE
  ![image](https://github.com/user-attachments/assets/9ffdc75c-099a-487f-ba85-d745fdc76920)

![image](https://github.com/user-attachments/assets/ff2bc94c-d8ad-4ddc-a0d1-fee24de0788a)

OPERATORS WE CAN PUT INTO 
  
- ! EXPRESSION	       The EXPRESSION is false.
- -n STRING      	The length of STRING is greater than zero.
-  -z STRING	    The lengh of STRING is zero (ie it is empty).
- STRING1 = STRING2	      STRING1 is equal to STRING2
- STRING1 != STRING2	       STRING1 is not equal to STRING2
- INTEGER1 -eq INTEGER2	    INTEGER1 is numerically equal to INTEGER2
- INTEGER1 -gt INTEGER2	    INTEGER1 is numerically greater than INTEGER2
- INTEGER1 -lt INTEGER2	    INTEGER1 is numerically less than INTEGER2
- -d FILE	FILE exists and is a directory.
- -e FILE	FILE exists.
- -r FILE	FILE exists and the read permission is granted.
- -s FILE	FILE exists and it's size is greater than zero (ie. it is not empty).
- -w FILE	FILE exists and the write permission is granted.
- -x FILE	FILE exists and the execute permission is granted.

 **NOTE:= is slightly different to -eq. [ 001 = 1 ] will return false as = does a string comparison (ie. character for character the same) whereas -eq does a numerical comparison meaning [ 001 -eq 1 ] will return true**

### NESETED IF
```bash
#!/bin/bash
# Nested if statements
if [ $1 -gt 100 ]
then
echo Hey that\'s a large number.
if (( $1 % 2 == 0 ))
then
echo And is also an even number.
fi
fi
```
### IF-ELSE 
```bash

if [$# -eq 1]
else.sh
#!/bin/bash
# else example
if [ $# -eq 1 ]
then
nl $1
else
nl /dev/stdin
fi
```
### IF - ELIF - ELSE
```bash
if [ <some test> ]
then
<commands>
elif [ <some test> ]
then
<different commands>
else
<other commands>
fi
```
-- Bollean operator is also allowed 

