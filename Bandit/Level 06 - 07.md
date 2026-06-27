# Bandit Level 6 -> 7

## Level Goal

The password for the next level is stored somewhere on the server and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Solution

First we login to the `bandit6` machine using ssh:

![login](../Images/Bandit/Level%206%20-%207/login.png)

Then we can `ls` command but it didnt return anything. So we check the condition given in the goal description.

It says that the required file has three characterstics:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

So we can use the `find` command to locate the file. Lets first find the flags needed to achieve this task so we run `man find`:

- The first flag we need is to specify that the thing being searched is a file, so for that we can use the `-type f` command:

    ![file type](../Images/Bandit/Level%206%20-%207/file%20flag.png)

- Secondly the file should be owned by the user `bandit7` so for that we can use the `-user <uname>` flag:

    ![user flag](../Images/Bandit/Level%206%20-%207/owner%20user.png)

- Thirdly, the file should belong to the user group `bandit6`. So we can use the `-group <gname>` flag for that:

    ![group flag](../Images/Bandit/Level%206%20-%207/owner%20group.png)

- And finally, the file size should be 33 bytes so we can use the `-size 33c` flag (where c specifies the size unit as bytes):

    ![size flag](../Images/Bandit/Level%206%20-%207/size%20flag.png)

So the final command we are going tos use will look like this:

`find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null`

Here:

- `/` specifies the search over the whole system
- `2>/dev/null` To ignore errors that may be displayed due to access limitations. (`2` stands for stderr, `>` is the redirection opeartor and `/dev/null` is special device file that discards anything written to it)

![find command](../Images/Bandit/Level%206%20-%207/find%20command.png)

Now we can simply use `cat` to extract the required password:

![password exttraction](../Images/Bandit/Level%206%20-%207/password%20extraction.png)

---


