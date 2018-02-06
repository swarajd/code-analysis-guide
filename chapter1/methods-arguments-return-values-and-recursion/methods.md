# Methods

In java, a method is a _named_ set of code that can be called \(invoked\) at any point in a program simply by utilizing the method's name. Think of a method as a subprogram that acts on data \(if any\) and often returns a value.

Each method has it's own name. When that name is encountered in a program, the execution of the program branches to the body of that method. When the method is finished, execution returns to the area of the program code from which it was called, and the program continues on to the next line of code.

\(source: [https://mathbits.com/MathBits/Java/Methods/Lesson1.htm\](https://mathbits.com/MathBits/Java/Methods/Lesson1.htm\)\).

Let's look at some examples of methods:

```
/*
    this method
    - returns an int
    - takes no parameters
*/
int getAnInteger() {
    return 6;
}

int a = getAnInteger(); // a == 6



/*
    this method
    - returns a string
    - takes two parameters
*/
String greetPerson(String prefix, String, lastName) {
    return "Hello, " + prefix + " " + lastName;
}

String greeting = greetPerson("Mr.", "Dhumne"); // greeting.equals("Hello, Mr. Dhumne")
```



