# First script

We have covered the background, now we are going to work through creating a first script. At the command prompt, type the command;

````linux
echo $USER
````

This command takes the environment variable __USER__ and echoes it to standard output e.g. the screen. Every user has a user/password combination in a file called __/etc/passwd__ and these entries also store data relating to your group and login shell.

We could use __grep__ to find it. Try the command

````linux
grep $USER /etc/passwd
````

This will take your user name as a search parameter and look for it in the password file.

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig6.jpg">
<figcaption>Fig 6. Nano editor.</figcaption>
</figure>

We can take this simple command and include it in a file which we can then run. Make a directory called __scripts__ and then make this you’re working directory. All future scripts will be stored here!

Using __nano__, create the following text file (change the editor name etc. to match your own) and call it __script1.sh__

The hash symbol (#) introduces a comment; this line is not further processed.

````linux
# By: John O'Raw
# Date: 17NOV10
# Function: show the users entry in the password file
# Script: script1
grep $USER /etc/passwd
exit 0
````

Now do an __ll__ to make sure the file is there. The editor just creates text files, we need to change the permissions on the file to make it executable.
Try the command

````linux
chmod u+rx script1
````

Now do another __ll__.

What happened?

To run our first script, we have one more problem!

Our script directory is not in the path, so if we try to run it, the shell will search for the script and not find it, even though we are in the working directory with the script. To run we need to tell the shell to run it from the working directory. Try the command;

````linux
./script1.sh
````
