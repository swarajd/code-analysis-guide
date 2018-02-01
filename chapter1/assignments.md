# Assignments, Increments, and Decrements

### Assignments

You've probably seen me use assignments all throughout this book already, when I do something like this:

```
int a = 6;
```

When you use that single `=` operator, you are assigning the value of `6` to the integer `a`. That's all well and good, but there are many other assignment operators that can be used. If you have read the "Operator Precedence and Associativity" chapter, you'll remember the chart that had the precedence of all the operators. On that chart was level 1, which contains all assignment operators, and looks like this:

![](/assets/assignment_operators.png)

Aside from the regular `=` operator, each one of these operators does the following:

```
int a = 6;

a += 3;    // a = a + 3
a -= 3;    // a = a - 3
a *= 3;    // a = a * 3
a /= 3;    // a = a / 3
a %= 3;    // a = a % 3
a &= 3;    // a = a & 3
a ^= 3;    // a = a ^ 3 
a |= 3;    // a = a | 3
a <<= 3;   // a = a << 3
a >>= 3;   // a = a >> 3
a >>>= 3;  // a = a >>> 3
```

#### Exercises

These exercises will all be in code blocks

```
// 1. 
int one = 9;
one += 4;

// what is the value of 'one': ____ ?



// 2. 
int two = 13;
two /= 6;

// what is the value of 'two': ____ ?



// 3. 
int three = 35;
three &= 11;

// what is the value of 'three': ____ ?



// 4.
int four = 2;
four <<= 3;

// what is the value of 'four': ____ ?



// 5. 
int five = 6;
five |= 7;

// what is the value of 'five': ____ ?



// 6.
int six = -300; //assuming a 32-bit integer
six >>>= 25

// what is the value of 'six': ____ ?
```





