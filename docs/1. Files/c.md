# Permissions

I am not digging deep here, this is just enough information for scripters!

Some form of basic file permissions exists consistently in all forms of UNIX, based on a very early draft of the POSIX standard. There are three scopes where permissions were applied: user, group, and others. The owner of a file can be changed using the __chown__ command and the group can be changed using __chgrp__. Look these commands up and understand how to use them.

Every filesystem object is

- Owned by a user (U) and has permissions that relate specifically to that user.
- Assigned to a group (G) which has specific permissions.
- Accessible by any other (O) user, dependent on specific permissions.

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig1.jpg">
<figcaption>Fig 1. Permissions example.</figcaption>
</figure>

Permissions are very simple, read (R), write (W), and execute (X) and in original UNIX systems were represented using octal codes.

<figure>
<img src = "https://jor-donegal.github.io/LinuxScripts26/images/fig2.jpg">
<figcaption>Fig 2. Permissions octal codes.</figcaption>
</figure>

When I write a script, I will often give it permissions of __755__. This allows me as the owner to read, write and execute. It allows anyone else to read and execute, but not to change my script!

There is an alternative way to do this using symbolic representation. To add read permission for a group, you could just use the command 

__chmod g+r filename__

To remove the execute permission for others, you could use the command

__chmod o-x filename__

For each permission (R, W, X) and each entity (U, G, O) you can either allocate (+) or remove (-) the specific permission.

From 1997 onwards, more complex ACLs were introduced to Unix via the POSIX standards. I won’t be covering these in this note set.
