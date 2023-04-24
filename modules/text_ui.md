# User interactions in text

pretty simple chapter here.

We will be going over 2 commands:

``` c++
cout;
// or
printf() // this isnt preferred in c++, its only here because it's used in c
```

``` c++
cin;
scanf(); // same deal with printf
```

To start, we need to import some packages into our program:

``` c++
#include <iostream> // for cin and cout

using namespace std;
/*
This command is entirely optional. what this does is it shortens our commands from:
std::<command>
to:
<command>
*/
```

![This article](https://www.w3schools.com/cpp/cpp_syntax.asp) explains everything we just did very well

## cout

similar to other languages like c++, c++ has a way to display text.

``` c++
cout << "Hello World" << endl;
```

will display the following:

```Hello World```

pretty simple.

note 2:

c++ does not create a newline character after printing, so having ```endl``` after your text is needed.

## Input

Input is also very simple:

``` c++
cout << "foo: ";
string input;
cin << input;
```

If we run this, the code will display ```foo:``` and pause for user input.

The user needs to type something and press enter like so:

``` shell
foo: bar
```

Now, we can do this:

``` c++
cout << input << endl;
```

and this will print ```bar```.
