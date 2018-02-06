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

Aa you can see, this function calls itself inside the `else` statement. 



