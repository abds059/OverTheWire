# Bandit Level 0

## Level Goal

The goal of this level is for you to log into the game using SSH. The 

- Host: bandit.labs.overthewire.org
- Port: 2220
- Username: bandit0 
- Password: bandit0

Once logged in, go to the Level 1 page to find out how to beat Level 1.

## Solution

Our task is to login to the machine using ssh. So we can utilize the following command based on the given info for ssh connection:

`ssh -p 2220 bandit0@bandit.labs.overthewire.org` 

After this command the connection will initiate and ask for password where we will use the password given above and the connection will be established.

![ssh connection for bandit0](../Images/Bandit/Level%200/Level%200.png)

---