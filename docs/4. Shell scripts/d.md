# Variables

Just about every programming language has a concept called a _variable_. This is normally a location in memory where a value can be stored (a number, a string of characters) and which has a symbolic name which can be used in programmes. Try the following example (don't put spaces around the equal sign, it won't work!!).

````linux
# By: John O'Raw
# Date: 24NOV19
# Function: Demonstrate the use of variables
# Script: script4
MY_MESSAGE="Good Morning!"
echo $MY_MESSAGE
exit 0
````

Every variable is saved as a string, so if you do try to add strings together, things won't work very well! Look at the __bc__ command; at the command prompt, type man __bc__ and read through.
In the example below, be careful with the quote symbol on line c=

On an Irish keypad, it’s the symbol above the tab key and to the left of the number one.

````linux
# By: John O'Raw
# Date: 24NOV19
# Function: Demonstrate the use of variables
# Script: script5
a=5.66
b=8.67
c=`echo $a + $b | bc`
echo "$a + $b = $c"
exit 0
````
