# terminal commands: part 1

## Prerequisites

none

## How to run terminal commands in python

In python, one of the built-in libraries, os, has a function called ```system``` which can be used to execute commands:

``` python
import os # will give us all of the functions from the os library

# echo is basically the terminal version of print
os.system("echo hello world")

# what this will show in terminal:
'hello world'

# what this will return:
0
```

The issue here is that os.system does not return the result of the command, but rather the exit code.

The solve for this is to use the ```subprocess``` module, and I have included a link for y'all to figure that out:

![link](https://stackabuse.com/executing-shell-commands-with-python/)

happy hunting!

corn
