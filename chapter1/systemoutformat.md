# System.out.format

I'll write out a quick guide as to how `System.out.format` works so that you guys can understand it.

The specifiers the test writers are limited to are:

```
%% = a percent sign
%n = a newline character
%c = a character
%d = an integer
%s = a string
```

Let's take a look at a few examples:

```
String st = "qwerty";
int num = 314;
char cha = "t";

System.out.format("there is a 10%% sale!\n"); // prints "there is a 10% sale!\n"
System.out.format("whoa%na new line!\n"); // prints the following:
/*
whoa 
a new line!\n
*/
System.out.format("fan%castic\n", cha); // prints the following: "fantastic\n"
System.out.format("I saved $%d today!\n", num); // prints the following: "I saved $100 today!\n"
System.out.format("the first few keys on my keyboard are %s\n", st); //prints what's below:
// "the first few keys on my keyboard are qwerty\n"


/*
    NOTE: when I type \n, I just mean newline, and I put it there to specify that there is one. You usually
    don't worry about it since you usually use System.out.println, which automatically places the new line
    there for you. I put it there deliberately because anything other than System.out.println most likely
    doesn't put the new line there for you.
*/
```



