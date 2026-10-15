# Selecting the shell

We have created our first script, but we need to add a bit more certainty!

There are many shells, we should start our scripts with a _sha-bang_ (# = sharp and ! = bang). This is the historical name for the head of the script which tells it which command interpreter to use. For all our practical sessions, we will be using bash, so our sha-bang command will be:

````linux
#!/bin/bash
````

Time for our second script. Call it __script2.sh__

````linux
#!/bin/bash
# By: John O'Raw
# Date: 17NOV10
# Function: Show users who are logged on
# Script: script2

echo "Welcome" $USER
echo "The following users are currently logged on"
who
exit 0
````

We are going to run this script a slightly different way. Rather than changing the file properties to executable we can run bash again and pass it a programme (our script!). Try the command;

````linux
bash script2.sh
````

You should be able to see all logged on users, probably just yourself!

So how did the previous shell script run without being executable? When we open a command prompt, we are running a process with the programme __/bin/bash__. To verify this, run the command __ps__. You will get a response back with the process id of the bash shell AND the process id (PID) of the __ps__ command you ran.

When I'm working as a systems admin, I may use the __last__ command to get a history of recent logins. The underlying log file this displays is at __/var/log/wtmp__
The last command has options for individual users, login time, etc. Read the related man page now.