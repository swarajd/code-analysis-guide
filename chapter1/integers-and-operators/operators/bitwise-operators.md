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
int b = ~a;    // once flipped, it becomes 11111001, or -7
```

#### Exercises

1. Assuming an integer only uses 8 bits, what is ~5?
2. Assuming an integer only uses 8 bits, what is ~26?
3. Assuming an integer only uses 8 bits, what is ~\(-7\)?
4. Assuming an integer only uses 16 bits, what is ~57?
5. Assuming an integer only uses 16 bits, what is ~115?
6. Assuming an integer only uses 16 bits, what is ~\(-550\)?

### And

The and operator takes two integers, and applies an AND to each of their bits, to further explain what an AND is, let me show you this diagram:

| first bit | second bit | result |
| :--- | :--- | :--- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

As you can see, when you apply an AND to two bits, the result will only be 1 if both bits are 1 already. Lets look at a few examples of this in practice.

```
int a = 9;     // 9 in binary is 00001001 
int b = 5;     // 5 in binary is 00000101
int c = a & b; // if you AND each bit, you'll get 00000001, which is 1
```



