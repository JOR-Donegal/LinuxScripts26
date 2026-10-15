# Test and Numbers

Normally when we type a command, the shell executes a fork and allows the program called by the command to execute in its own process. However, there are a range of commands built into the shell, which reasonably enough are called built-ins. To review the built in  commands in the bash shell, type the command __info bash__ and select __Shell Built In Commands__ and press [return].

When we looked at flow control we came across the test builtin in combination with if. The test builtin command returns 0 (True) or 1 (False) depending on the evaluation of an expression. You can also use square brackets.

__test expr__ and __[ expr ]__ are equivalent.

You can examine the return value by displaying __$?__

Try typing the command

````linux
test 3 -gt 4 && echo True || echo false
````

You have just asked the shell to "test if the number 3 is greater than the number 4, if 0 echo True, if 1 echo False", and -gt checks for the case greater than.
There are a range of mathematical tests we can run.

-eq is equal to 
- 5 == 6 
- if test 5 -eq 6 
- if [ 5 -eq 6 ]

-ne is not equal to 
- 5 != 6 
- if test 5 -ne 6 
- if [ 5 -ne 6 ]

-lt is less than  
- 5 < 6 
- if test 5 -lt 6 
- if [ 5 -lt 6 ]

-le is less than or equal to 
- 5 <= 6
- if test 5 -le 6 
- if [ 5 -le 6 ]

-gt is greater than 
- 5 > 6 
- if test 5 -gt 6 
- if [ 5 -gt 6 ]

-ge is greater than or equal to 
- 5 >= 6 
- if test 5 -ge 6 
- if [ 5 -ge 6 ]

We also have logical test where
- ! means NOT
- -a means AND
- -o means OR

Let's try some calculations! Remember, the quote around the expr is the one above the tab on the top left of the keyboard!!

````linux
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Calculations
# Script: script15

echo "This script check to see if the first argument is bigger than the second"

# Check to see if we have two arguments
if [ $# -ne 2 ]
then
  echo "Usage - $0 x y"
  echo "Where x and y are summed"
  exit 1
else
  echo "$1 plus $2 is `expr $1 + $2`"
fi
 
exit 0
````

We are going to be a bit more sophisticated in our use of IF-THEN-ELSE. We have a test option __elif__ which means ELSEIF. It allows us to check for additional tests.

````linux
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Calculations
# Script: script16

if [ $# -ne 1 ]
then
  echo "Usage - $0 x"
  echo "Where x will be tested"
  exit 1
fi

echo "This script checks one argument"

if [ $1 -lt 0 ]
then
  echo "$1 is less than zero"
elif [ $1 -eq 0 ]
then
  echo "$1 is zero!"
elif [ $1 -gt 0 ]
then
  echo "$1 is greater than zero"
fi
exit 0
````