# Bandit Level 5 -> 6

## Level Goal

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

## Solution

So first we login into the machine `bandit5`.

![login](../Images/Bandit/Level%205%20-%206/login.png)

Then we run `ls` to view avaiable directories and files. Here we see `inhere` directory and enter inside that using `cd` command. 

![inhere dir](../Images/Bandit/Level%205%20-%206/inhere%20dir.png)

Inside the directory we are given a number of sub directories. 

So lets review the Level Goal statement:

The file should be:

- human readable
- 1033 bytes in size
- not executable

So we have to find a file that contains these properties. So we can use the `find` command to search for the required file.

First we can gather the relevant flags needed to form the final command. So we can run `man find` to search for them:

- For the human readable part we discovered a flag `-type f`:

    ![human readable](../Images/Bandit/Level%205%20-%206/regular%20file.png)

- For specifying the 1033 bytes size we found a flag `-size n`:

    ![size flag](../Images/Bandit/Level%205%20-%206/size%20flag.png)

- And finally to match the not executable condition we can use the `-executable` flag with `!` operator:

    ![executable flag](../Images/Bandit/Level%205%20-%206/executable%20flag.png)

So the final command becomes:

`find -type f -size 1033c ! -executable`

(where c specifies the size unit as bytes)

![find command](../Images/Bandit/Level%205%20-%206/find%20command.png)

Now we can simply use `cat <filename>` to retrieve the password:

![password extraction](../Images/Bandit/Level%205%20-%206/password%20extraction.png)

---

