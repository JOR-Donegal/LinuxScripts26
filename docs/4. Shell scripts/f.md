# Exit Codes

When a process terminates in Linux, it returns an eight-bit code to the parent process.

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig7.jpg">
<figcaption>Fig 7. Return code.</figcaption>
</figure>

When we run a command in the shell, it always returns an exit code. To get the exit code of the previous command type;

````linux
echo $?
````

at the command prompt.

The next thing I have done is to try to run __cat__ against a non-existent file.

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig8.jpg">
<figcaption>Fig 8. Return code 1.</figcaption>
</figure>

The __cat__ command returns a message to STDOUT (the screen) informing me that the attempt failed. What I don’t normally see is that it also returned a “1” to the shell. We can use this information as the basis for conditional branching and decision making in scripts.

Finally, we also explain the line

````linux
exit 0
````

in all the previous sample scripts, we are unconditionally exiting with a success (0) being returned to the shell. We could make decisions in the script and return other values to the shell.
We can provide user-specific return codes, but some codes have been standardized and should only be used for their intended purpose. Check the standardized codes now.
