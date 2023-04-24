# tips for navigating filesystems

In this project (and all c++ projects because this language loves to be annoying) we want to stick to standard libraries.

The reason for this is because c++ has one funny (and very frustrating) quirk in not having native package support.

(for example, in node.js we have ```npm``` and python has ```pip```)

what this means is that a lot of the time, in order to use external libraries we need to copy the code into our folders, which is messy and annoying.

An exception to this is the win32 library.

## STD libraries pertaining to filesystems

### Reading/Writing Files

if we want to simply read files, we can use ```cin``` from our handy ```iostream``` library that we discuss in the ![text ui module]().

```cout``` can be used in a similar fashion.

### Navigating Directories

This is where it gets harder as this is much less common to do.

I found a library called ```filesystem``` that may be the answer to our problem.

See the StackOverflow answer that I found ![here](https://stackoverflow.com/questions/612097/how-can-i-get-the-list-of-files-in-a-directory-using-c-or-c/37494654#37494654)

A big part of this project will be researching how to do stuff, so I will leave this to other project members to figure out how to do this.
