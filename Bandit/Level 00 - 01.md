# Bandit Level 0 -> 1

## Level Goal

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Solution

In order to proceed to level 1 we need to extract the password stored on the machine. So we can simply list down all available files in the current directory using `ls` command. We can see the directory has only one file named `readme`. Then we use `cat` to extract the content of the file on the terminal. This will give us the password for the next machine.

![bandit1 password](../Images/Bandit/Level%200%20-%201/Level%200%20-%201.1.png)

After we use ssh to login to level 1 through username `bandit1` and the extracted password:

![bandit1 ssh](../Images/Bandit/Level%200%20-%201/Level%200%20-%201.2.png)

---
