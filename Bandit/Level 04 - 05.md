# Bandit Level 4 -> 5

## Level Goals

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## Solution

First we login to the level 4 machine using the password obtained in the previous level.

![login](../Images/Bandit/Level%204%20-%205/login.png)

Then we run `ls` to see available directories and find a directory named `inhere` and move into that directory through `cd`. Then we list down the files inside that directory using `ls`.

We can see 10 files there. According to the level goal the password is within one of these file and that file is human readable. So we simply use `cat ./<filename>` sequentially until we find the password in the file `-file07`:

![password](../Images/Bandit/Level%204%20-%205/password.png)

---