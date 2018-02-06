# Control Flow

In this section, I'll be going over the most common control flow operator: `if/else` . This operator basically executes one section of code, or another, depending on a condition. Let's look some examples below:

```
/// Ex 1.

int b = 5;
int a = 6;

if (a == 6) {
    b = 4;
}

// b == 4



/// Ex 2.

int c = 8;
int d = 2;

if (d == 3) {
    c = 9;
} else {
    c = 0;
}

// c == 0



/// Ex 3.

int e = 4;
int f = 3;
int g = 1;

if (f == 9) {
    g = 10;
} else if (f == 3) {
    g = 11;
} else {
    g = 12;   
}

// g == 11

```

The way an if-statement works, is that inside the parentheses, you place an expression that evaluates to a boolean value. It's relatively simple to understand, as you basically check if the expression evaluates to true, and if it does, you execute the code inside that if-block, otherwise you either move on to the else-if or else block \(if there is one\), or move on with the rest of the code. 

