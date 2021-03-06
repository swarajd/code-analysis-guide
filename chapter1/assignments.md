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

### Increments

Increments are used if you want to shorten the process of incrementing an integer \(or any numeric value\) by 1. They can be used in two ways: pre-increment `++a` or post-increment `a++` . For this event, order does not matter at all. Let's see how this operator is used.

```
int a = 6;
a++; // a == 7

a = 6;
++a; // a == 7
```

#### Exercises

```
// 1. 
int a = 10;
a++;

// What is 'a' now: ___ ?




// 2.
int a = 7;
++a;

// What is 'a' now: ___ ?
```

### Decrements

Decrements are literally the same as increments, except they use `--` and they decrease the integer \(or any numeric value\) by 1. Here are some exercises.

#### Exercises

```
// 1. 
int a = 5;
a--;

// What is 'a' now: ___ ?



// 2.
int a = 11;
--a; 

// What is 'a' now: ___ ?
```









