# User interactions in text

pretty simple chapter here. 

We will be going over 2 commands:

``` python
print()
```

``` python
input()
```

## Print

similar to other languages like c++, python has a way to display text.

``` python
print("hello world")
```

will display the following:

```hello world```

pretty simple.

note: the c++ equivalent would be either of the following:

``` c++
std::cout << "hello world" << std::endl;
std::printf("hello world\n")
```

note 2:

python creates a newline character after printing, so having ```\n``` after your text is not needed.

## Input

Input is also very simple:

``` python
user_input = input("foo: ")
```

If we run this, the code will display ```foo: ``` and pause for user input.

The user needs to type something and press enter like so:

``` shell
foo: bar
```

Now, we can do this:

``` python
print(user_input)
```

and this will print ```bar```.
