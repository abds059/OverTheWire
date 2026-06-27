# Bandit Level 3 -> 4

## Level Goal

The password for the next level is stored in a hidden file in the inhere directory.

## Solution

Here we have to find password for level 4 machine. So we first login through the password we got earlier.

![login](../Images/Bandit/Level%203%20-%204/login.png)

Then we use `ls` to list down available directories and files. We can see there is only one directory called `inhere`, so we use `cd` to move inside that directory.

![inhere dir](../Images/Bandit/Level%203%20-%204/inhere%20dir.png)

Here we tries to use `ls` but no files were displayed. This means that if the directory is not empty there can be some hidden files (files that start with `.`).

So lets check the available help given for this level specifically the `ls` one. Clicking on `ls` on the webpage it will direct us to `ls` man page of Ubuntu.

![ls man](../Images/Bandit/Level%203%20-%204/ls%20man.png)

Here we can see the option of `-a` for displaying hidden files. So we use this and we can see a file named `...Hidden-From-You`. To confirm its permissions and exact name we can use the command `ls -la`. 

Now we can simply extract the password by using the command: `cat ./<filename>`:

![password](../Images/Bandit/Level%203%20-%204/password.png)

---

