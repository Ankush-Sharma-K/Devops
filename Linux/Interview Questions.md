# 1) Why the user management is necessary?
Because of accountability, because of user management we can find the history of every activity who did it.


# 2) What is difference between Useradd and adduser?
### Useradd
```bash
useradd
```
It is a very basic command used to create a new user in linux. But there are few **limitations of this command** 
is that it does not create any home directory for the user. It just creates the user.
Also it is **usefull in some cases** Like:
When ever we are writing a script and we have to create a user at that time we don't want the terminal to be interactive in between the script,
so we use this so that all things go smoothly.
**But if you want to add home directory**
### Add while creating user:
```bash
sudo useradd -m
```
```bash
sudo useradd -m -s /bin/bash -c "Comment" username
```
*** -m: Add home directory.
-s: sets the bash as default shell
-c: Adds the comment.***

### Add home directory for the existing user:
```bash
sudo mkhomedir_helper username
```

### To Check the user is created or not:
```bash
/etc/passwd
```
if a entry is there of the username that means the user is created.

### Adduser
```bash
sudo adduser username
```
It is an interactive command which will ask all necessary information while creating the new user.
*Creates a home directory automatically.

*Asks for the password.  
*Less suitable to use in scripts.

# 3) Is it possible to restore the old password of a User in Linux? Or
## You have access to a linux machine can you recover the passwords of all users on that machine.
All passwords are stored in encrypted form at:
```bash
/etc/shadow
```
It is nearly impossible to decrypt these passwords.
