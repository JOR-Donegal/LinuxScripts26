# Seq

When we are iterating through a list, the seq command can be very handy. Go to the command prompt and type 

````linux
seq 10
````

Very handily, it has iterated through numbers from 1 to 10.

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig9.jpg">
<figcaption>Fig 9. Seq command.</figcaption>
</figure>

In a case where I want to iterate through something, this gives me nice, tight code.
Consider the script below where I use indexnumber as a variable. 

````linux
#!/bin/bash
# By: John O'Raw
# Date: 27NOV19
# Function: Simple number check
# Script: script11

for indexnumber in ‘seq 10’
do
    touch TextFile$indexnumber.txt
done
````

The result will be

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig10.jpg">
<figcaption>Fig 10. Seq script.</figcaption>
</figure>