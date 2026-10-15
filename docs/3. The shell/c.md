# Options

Consider the __ls__ command.

__ls__ is a single command which gives a listing of the working directory.

__ls -l__ is a single command with one option specified which gives a long listing of the working directory.

ls worked a bit different from copy. Rather than having arguments is has options. Options are a special type of argument which modify the behavior of a command. With most commands, the options come first and then the arguments.

For example, what does the command

````linux
ls -l *.txt
````

do?

One special case is the command option __--help__ which can be very useful to get help!

For example, try

````linux
ls --help
````

In some case we may need to string multiple options together. Try the following sequence of commands.

````linux
ls -i
ls -l
ls -il
````

The two options are concatenated and __ls__ does both.
