# Binary Operators

These should also be pretty easy to get, but there are some subtleties, which I will cover in this section. The five operators that will be used are the following: `+, -, *, /, and %`.

### Addition

Addition is very simple, but it can become ugly quickly. In the common case, you will have two integers, and once you add them you will get a regular result. Let's say we have the following:

```
int a = 56;
int b = 9;
int c = a + b; // 65
```

This is normal enough, but there is one edge case I urge you to look out for:

```
int a = 2147483647;
int b = 1;
int c = a + b; // -2147483648
```

That doesn't seem right, it returned a negative number! Well, if you remember from the previous section, $$2147483647$$ is the largest positive value the integer value can take, and it's binary representation is the following: `01111111111111111111111111111111`. If you add 1 to that, it's binary representation will be `10000000000000000000000000000000`. This is equal to the smallest integer value, or $$-2147483648$$.

### Subtraction

Subtraction is also very simple, and has the same ugliness as addition. In the common case, you will have two integers, and once you subtract them, you will get a regular result. Let's say we have the following:

```
int a = 56;
int b = 9;
int c = a - b; // 47
```

This is normal enough, but let's refer back to the edge case in the addition section.

```
// c = -2147483648
int d = 1;
int e = c - d; // 2147483647
```

This is even weirder, it returned a positive number! This is similar to above in that if you fiddle around with binary you'll see that you go from `10000000000000000000000000000000`to `01111111111111111111111111111111`.

### Multiplication

Multiplication holds the same edge cases as addition.

### Division

Integer division in java can seem tricky, but once you understand it, it becomes relatively simple. The way integer division works in java is that java basically divides the two numbers, gives you the quotient, and throws away the remainder. Lets look at a few examples:

```
int a = 1 / 3;   //  0
int b = 4 / 3;   //  1
int c = 11 / 3;  //  3
int d = -6 / 3   // -2
ind e = -5 / 3   // -1
int f = -8 / -2  //  4
```

#### Exercises

1. 13/3
2. 89/11
3. 27/6
4. 74/9
5. 123/7
6. 16/3

### Modulus

The modulus operator looks like this: `%`. The modulus operator gives you the remainder between two numbers if you divide them. Lets look at a few examples:

```
int a = 1 % 3;  // 1
int b = 4 % 3;  // 1
int c = 11 % 3; // 2
int d = -6 % 3; // 0
int e = -5 % 3  // -2
int f = -8 % -2 // 0
```

#### Exercises

1. 17 % 3
2. 87 % 11
3. 28 % 6
4. 77 % 9
5. 121 % 7
6. 19 % 3



