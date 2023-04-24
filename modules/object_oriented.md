# Imlplementing OOP

OOP (Object Oriented Programming) is the main difference between the languages C and C++.

OOP is VERY IMPORTANT TO KNOW (it is the point behind the main CS series classes at FHDA)

So, how do we do OOP?

## What Is OOP?

OOP is a way for us to implement our own variable types.

Examples of the basic variables we already have are:

* ```Ints```
* ```Chars```
* ```Arrays```

We also have some objects that some people may have already used before in c++. Two very common examples are ```string``` and ```vector```.

## Enums

An enum is our own variable type, and the most basic thing we will cover.

These originate in the c language.

``` C++
#include <iostream>
using namespace std;

enum day{Mon, Tue, Wed, Thurs, Fri, Sat, Sun};

// now we can use this like so:

int main() {
    enum day first = Mon;

    enum day second = Tue;

    if (first == second) {
        cout << "true" << endl;
    } else {
        cout << "false" << endl;
    }
    
    return 0;
}
```

this would display the following:

``` shell
false
```

for more info, ![check this out!](https://www.geeksforgeeks.org/enumeration-enum-c/)

## Structs

Structs are similar to objects, except they lack some core functionality we will explain later.

Structs allow us to have a variable that stores multiple values in itself. For example:

``` c++
#include <iostream>
using namespace std;

struct person {
    int age;
    string name;
};

int main() {
    struct person person1; // initializing our person

    // we can put in the values like so:
    person1.age = 22;
    person1.name = "Doug Dimmadome";

    // we can now access these values the same way:

    cout << person1.name << ", " << person1.age << endl;
}
```

this will print:

``` shell
Doug Dimmadome, 22
```

For more info, ![read here.](https://www.w3schools.com/c/c_structs.php)

note: the string stuff may be incorrect.

## Classes

Classes are our actual objects! (WOOOO)

Classes are very similar to structs, but are *slightly* different.

The big difference is that they can have their own functions, called methods.

Common methods are setters and getters.

### Setters

Set a variable to a value

### Getters

Return the value of the variable

The main reason for setters and getters is to make sure that our values for variables are accurate.

``` c++
#include <iostream>
#include <string> // for to_string()
using namespace std;

class Person { // we capitalize class names in c++ because its coding convention
    private: // the user cannot see or modify the stuff in private
        int age;
        string name;

    public: // the user can see and modify the stuff in public
        Person() {
            /*
            This is our default constructor. This constructor will be called 
            when we initialize the variable without any data. Will show below.
            */
            age = 0;
            name = "John Doe";
        }
        Person(int age, string name) {
            /*
            This is our second constructor, and we can call it like a function 
            to initialize our variable for us. Will also show below.

            we will use our setters, defined below in this function 
            to validate our inputs
            */
            
            bool valid = set_age(age);
            if (!valid) {
                throw "Invalid age: age must be above 0"; // an error message
            }
            set_age(age);
        }

        // our setters
        bool set_age(int age) {
            if (age < 0) {
                return false; // we do not want negative ages
            }
            this.age = age; // this.age is the value saved in this object
            return true;
        }
        
        bool set_name(string name) {
            // no validation needed here
            this.name = name;
            return true;
        }

        /*
        an alternative to returning boolean values would be to throw an 
        exception (to do an error message) like we do in the constructor but 
        that is a bit advanced for a simple tutorial right now.
        */

        // our getters
        int get_age(int age) { return this.age; }
        string get_name(string name) { return this.name; }

        // we can also have other functions, for example to_string()

        string to_string() {
            return this.name + ", " + to_string(this.age);
        }
};

int main() {
    Person person1; // default constructor
    person1.set_name("John Smith");
    person1.set_age(30);

    Person person2 = new Person("John Smith", 30); // second constructor

    // both of these have the same result

    // we can now print the value of our person:

    cout << person1.to_string() << endl;

    // note: we cannot do this:
    cout << person1 << endl;

    // that requires additional code that I won't explain here
}
```
