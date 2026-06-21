# Bandit Level 1 - 2

## Level Goal

The password for the next level is stored in a file called `-` located in the home directory

## Solution

On the bandit1 machine we first use `ls` to list down available files. We can see a file named `-` in the current directory. In order to get the content of this file, we can try using `cat <filename>`. But this didnt yield any result. 

So, we can check out the help links given to us. Let us explore the first link given to us (Google Search for “dashed filename):

![syntax search through give help link](../Images/Bandit/Level%201%20-%202/Level%201%20-%202.2.png)

So the syntax to be used here is `cat ./-`. Lets proceed with this to extract the password:

![password extraction for bandit2](../Images/Bandit/Level%201%20-%202/Level%201%20-%202.1.png)

---