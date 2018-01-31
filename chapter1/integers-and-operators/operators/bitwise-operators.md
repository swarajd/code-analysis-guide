# Bitwise Operators

Bitwise operators are probably the trickiest operators to understand, as they require a deep understanding of bits. Thankfully, these operators can only take up 10% of the test, so you don't have to worry too much about this, but it's good to know this concept in general.

There are 7 bitwise operators in total: `~, &, |, ^, <<, >>, and >>>`. Their names are: negation, and, or, xor, left shift, arithmetic right shift, and logical right shift. If you don't have a solid foundation in bits, I suggest revisiting the integers section and brushing up on how integers are represented in binary, or doing a bit of external research on that concept.

Lets go over each operator in detail.

### Negation

The negation operator is pretty simple. It flips all the bits of an integer. Lets look at a few examples:

```
int a = 7;     // 7 in binary is 00000000000000000000000000000111
int b = ~a;    // once flipped, it becomes 11111111111111111111111111111000, or -8
```

Lets take a look at some 8 bit examples

```
int a = 6;     // 6 in binary is 00000110
int b = ~a;    // once flipped, it becomes 11111001, or -7If
```

#### Exercises

1. Assuming an integer only uses 8 bits, what is ~5?
2. Assuming an integer only uses 8 bits, what is ~26?
3. Assuming an integer only uses 8 bits, what is ~\(-7\)?
4. Assuming an integer only uses 16 bits, what is ~57?
5. Assuming an integer only uses 16 bits, what is ~115?
6. Assuming an integer only uses 16 bits, what is ~\(-550\)?

### And

The _and_ operator takes two integers, and applies an AND to each of their bits, to further explain what an AND is, let me show you this diagram:

| first bit | second bit | result |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

As you can see, when you apply an AND to two bits, the result will only be 1 if both bits are 1 already. Lets look at an example of this in practice.

```
int a = 9;     // 9 in binary is 00001001 
int b = 5;     // 5 in binary is 00000101
int c = a & b; // if you AND each bit, you'll get 00000001, which is 1
```

If you're confused, look at this table:

| number | bit 1 | bit 2 | bit 3 | bit 4 | bit 5 | bit 6 | bit 7 | bit 8 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 9 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 1 |
| 5 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |

If you look at the first table and apply the logic to each column of this table, you'll see how I get the result of 1.

#### Exercises

1. 13 & 6?
2. 5 & 7?
3. 2 & 10?
4. 25 & 19?
5. 13 & 29?
6. 11 & 13?

### Or

The _or_ operator is similar to the _and_ operator, but it follows different rules. Lets look at this diagram to see what the rules are:

| first bit | second bit | result |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

As you can see, when you apply OR to two bits, the result will be 1 if at LEAST 1 of the bits is 1. Lets look at an example of this in practice.

```
int a = 9;     // 9 in binary is 00001001
int b = 5;     // 5 in binary is 00000101
int c = a | b; // if you OR each bit, you'll get 00001101, which is 13
```

#### Exercises

1. 13 \| 6?
2. 5 & 7?
3. 2 & 10?
4. 25 & 19?
5. 13 & 29?
6. 11 & 13?

### Xor

The _xor_ operator is similar to the _or_ operator, but it's a bit more particular. Lets look at this diagram to see what the rules are:

| first bit | second bit | result |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

It's not immediately obvious, but the result is only 1 when ONLY 1 of the bits is set to 1. Lets look at an example of this in practice.

```
int a = 9;     // 9 in binary is 00001001
int b = 5;     // 5 in binary is 00000101
int c = a ^ b; // if you XOR each bit, you'll get 00001100, which is 12
```

#### Exercises

1. 13 ^ 6?
2. 5 ^ 7?
3. 2 ^ 10?
4. 25 ^ 19?
5. 13 ^ 29?
6. 11 ^ 13?

### Left Shift

If you're not used to bitwise operators, this operator probably looks really confusing. No, this doesn't mean MUCH greater than, it means you shift the bits of a number by a certain amount. Lets look at some examples:

```
int a = 9;      // 9 in binary is 00001001
int b = 2;      // the number of bits to shift
int c = a << b; // 36
/*
    What we're doing here is shifting the bits to the LEFT by two bits.
    On the right end, we place 0s for every bit we shift to the left, and chop
    off the same number of bits on the left.
    So we had 00001001, but now we have 00100100, which is 36
*/

int d = 150;    // 150 in binary is 10010110
int e = 3;      // the number of bits to shift
int f = d << e; // 144
/*
    we shifted this number to the left by 3,
    so we had 10010010, but now we have 10010000, which is 144
*/
```

If the concept of shifting by bits is confusing, you can also think of it like this: If you have something like `9 << 3`, then you can think of it like $$(9 * 2^3) \& n$$. Where $$n = 2^k - 1$$, where $$k$$ is the number of bits that make up an integer.

#### Exercises

1. Assuming an integer only uses 8 bits, what is 205 &lt;&lt; 4?
2. Assuming an integer only uses 8 bits, what is -232 &lt;&lt; 2?
3. Assuming an integer only uses 8 bits, what is 16 &lt;&lt; 6?
4. Assuming an integer only uses 8 bits, what is -2 &lt;&lt; 5?
5. Assuming an integer only uses 8 bits, what is 7 &lt;&lt; 3?
6. Assuming an integer only uses 8 bits, what is -9 &lt;&lt; 2?

### Arithmetic Right Shift

Arithmetic Right Shift is similar to left shift, except it shifts bits to the RIGHT, AND it keeps the sign of the integer. Lets look at some examples:

```
int a = 25;     // 25 in binary is 00011001
int b = 2;      // the number of bits to shift
int c = a >> b; // 6
/*
    We shifted this number to the right by 2,
    so we had 00011001, but now we have 00000110, which is 6
*/

int d = -15;    // -15 in binary is 11110001
int e = 3;      // the number of bits to shift
int f = d >> e; // -2
/*
    we shifted this number to the right by 3,
    so we had 1110001, but now we have 11111110, which is -2
    Notice how since this number was negative, the left side
    was populated by 1s instead of 0s
*/
```

The concept of bit shifting in this scenario might be even more confusing than left shifts, but I would say try and understand what's really going on so you can be comfortable with how this operator works.

#### Exercises

1. Assuming an integer only uses 8 bits, what is 205 &gt;&gt; 4?
2. Assuming an integer only uses 8 bits, what is -232 &gt;&gt; 2?
3. Assuming an integer only uses 8 bits, what is 16 &gt;&gt; 6?
4. Assuming an integer only uses 8 bits, what is -2 &gt;&gt; 5?
5. Assuming an integer only uses 8 bits, what is 7 &gt;&gt; 3?
6. Assuming an integer only uses 8 bits, what is -9 &gt;&gt; 2?

### Logical Right Shift

Logical Right Shift is exactly the same as Arithmetic Right Shift, EXCEPT for the fact that a logical right shift will always populate the left with 0s instead of 1s, regardless of sign. Lets look at a previous example, but with logical right shift instead of arithmetic right shift.

```
int d = -15;     // -15 in binary is 11110001
int e = 3;       // the number of bits to shift
int f = d >>> e; // 14
/*
    we shifted this number to the right by 3,
    so we had 1110001, but now we have 00001110, which is 14
    Notice how even though this number is negative, the left
    side was populated by 0s
*/
```

#### Exercises

1. Assuming an integer only uses 8 bits, what is 205 &gt;&gt;&gt; 4?
2. Assuming an integer only uses 8 bits, what is -232 &gt;&gt;&gt; 2?
3. Assuming an integer only uses 8 bits, what is 16 &gt;&gt;&gt; 6?
4. Assuming an integer only uses 8 bits, what is -2 &gt;&gt;&gt; 5?
5. Assuming an integer only uses 8 bits, what is 7 &gt;&gt;&gt; 3?
6. Assuming an integer only uses 8 bits, what is -9 &gt;&gt;&gt; 2?



