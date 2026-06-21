# Bandit Level 2 -> 3

## Level Goal

The password for the next level is stored in a file called --spaces in this filename-- located in the home directory

## Solution

So we can simply first list down the available files in the directory using `ls`. We can see a file named `--spaces in this filename--`.

Now this file is a bit difficult to handle, as it contains `--` both at starting and ending as well there are spaces between the words. 

So lets first see what the help link tells us about this:

![help link](../Images/Bandit/Level%202%20-%203/level%202%20-%203.1.png)

So it basically tells us that for a filename with spaces we can do the following:

- We can either encode that filename within double qoutes like this for e.g,  `"spaces with space"`

- Or we can use `\` in place of spaces like this: `spaces\ with\ spaces`

- Also we can type first few letters of filename and press `Tab` for autocomplete.

![bandit3 password extraction](../Images/Bandit/Level%202%20-%203/level%202%20-%203.2.png)

So I tried a few combinations and this one succeeded and gave us the required password:

`cat ./--spaces\ in\ this\ filename--`

---