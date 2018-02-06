# Methods

In java, a method is a _named_ set of code that can be called \(invoked\) at any point in a program simply by utilizing the method's name. Think of a method as a subprogram that acts on data \(a list of parameters\) and often returns a value.

Each method has it's own name. When that name is encountered in a program, the execution of the program branches to the body of that method. When the method is finished, execution returns to the area of the program code from which it was called, and the program continues on to the next line of code.

\(source: [https://mathbits.com/MathBits/Java/Methods/Lesson1.htm\](https://mathbits.com/MathBits/Java/Methods/Lesson1.htm%29%29. \)

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

/*
    this method
    - returns a character array
    - takes one parameter
*/
char[] getCharArray(String str) {
    int len = str.length();
    char[] ret = new char[len];
    for (int i = 0; i < len; i++) {
        ret[i] = str.charAt(i);
    }
    return ret;
} 

char[] charArr = getCharArray("coding") // charArr == {'c', 'o', 'd', 'i', 'n', 'g'}
```

### Exercises

```
// 1.

int doMath(int a, int b, int c) {
    return a + b + c;
}

int d = doMath(3, 4, 5);

// what is the value of 'd': ___ ?




// 2.

int firstMethod(int a) {
    return a + 3;
}

int secondMethod(int b) {
    return b * 2;
}

int c = secondMethod(firstMethod(9));

// what is the value of 'c': ____ ?




// 3. 

int someMethod(int n) {
    return n * n;
}

int a = 0;

for (int i = 0; i < 5; i++) {
    a += someMethod(i);
}

// what is the value of 'a': _____ ?
```



