# Recursion

This lesson builds off of the previous lesson, and has to do with calling methods inside themselves \(which you CAN do by the way\). Let's look at a common example of recursion:

```
int factorial(int n) {
    if (n <= 0) {
        return 0; // we aren't dealing with 0 or negative numbers right this second
    } else if (n == 1) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
}
```

Aa you can see, this function calls itself inside the `else` statement. Let's look at how this code would execute.

```
int a = factorial(5);

/*
    when we first call it, we can see that n = 5, and that n is greater than 0 and it's not 1, 
    so it goes to the else statement.
*/

int a = 5 * factorial(4);

/*
    this basically repeats until n == 1
*/
int a = 5 * 4 * factorial(3);
int a = 5 * 4 * 3 * factorial(2);
int a = 5 * 4 * 3 * 2 * factorial(1);
int a = 5 * 4 * 3 * 2 * 1; // a == 120
```

That example was fairly linear, so lets look at a different example of recursion using the fibonacci sequence:

```
int fib(n) {
    if (n < 1) {
        return -1;
    } if (n == 1 || n == 2) {
        return 1;
    } else {
        return fib(n - 1) + fib(n - 2);
    }
}
```

This function is a bit more complex, since the `else` statement calls `fib` _twice_. Let's step through this code and see what happens.

```
int b = fib(7);

/*
    we know b isn't less than 1, and it's not 1 or 2, so we go to the else
*/

int b = fib(6) + fib(5);

/* 
    now you'll notice that there are two calls to fib, so you have to take care of two recursive calls at
    the same time. I'll model this in a tree to hopefully make it easier to read
*/ 

/*
fib7
├── fib5
│   ├── fib3
│   │   ├── fib1
│   │   │   └── 1
│   │   └── fib2
│   │       └── 1
│   └── fib4
│       ├── fib2
│       │   └── 1
│       └── fib3
│           ├── fib1
│           │   └── 1
│           └── fib2
│               └── 1
└── fib6
    ├── fib4
    │   ├── fib2
    │   │   └── 1
    │   └── fib3
    │       ├── fib1
    │       │   └── 1
    │       └── fib2
    │           └── 1
    └── fib5
        ├── fib3
        │   ├── fib1
        │   │   └── 1
        │   └── fib2
        │       └── 1
        └── fib4
            ├── fib2
            │   └── 1
            └── fib3
                ├── fib1
                │   └── 1
                └── fib2
                    └── 1

Now essentially what you'll do is take all the final values of 1 and add them all up.
If we manually do fibonacci, we'll see that we get the sequence: 1 1 2 3 5 8 13. 13 is the 7th number.
If we add up all the ones, we'll see we have 13 ones, which is also the 7th number. 
*/
```

### Exercises

```
// 1.

void collatz(int n) {
    System.out.println(n);
    if (n == 1) {
        return;
    } else if (n % 2 == 0) {
        collatz(n / 2);
    } else {
        collatz(n * 3 + 1);
    }
}

// What does collatz(10) print: _______________ ?



// 2.

void countdown(int i) {
    if (i <= 0) {
        System.out.println("blastoff!");
    } else {
        System.out.println(i);
        countdown(i - 1);
    }
}

// What does countdown(7) print:
------







------




// 3.

int power(int x, int n) {
    if (n > 1) {
        return x * power(x, n - 1);
    } else {
        return x;
    }
}

// What does power(3, 4) return: ____ ?

```



