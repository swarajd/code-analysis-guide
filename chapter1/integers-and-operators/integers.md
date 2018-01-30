# Integers

In java, an integer is a 32-bit signed two's complement integer. Integers have a minimum value of $$-2^{31}$$ or $$ -2147483648$$ and a maximum of $$2^{31} - 1$$ or $$2147483647$$.

This might be a bit overwhelming, so lets step through this sentence slowly \(And if it isn't overwhelming, read this page anyways, you might learn something new\).

> "32-bit"

What does it mean for a data type to have a certain number of bits? Well, lets go over the concept of a bit. In a computer, data is made up of bits, which are basically 1s and 0s. A bit is the smallest unit of memory in a computer. So, if a data type has 32 bits, it's represented using 32 bits in a row. So an integer can be represented as such: `11000010011011010110110111011111` . These bits basically read as binary, so we would convert this binary string to decimal.

If you don't know what binary is, binary is how you'd represent a number using 1s and 0s. It is also known as base-2. Lets talk about how to convert binary to decimal and back.

Normally, in base-10, also known as decimal, we have each digit be multiplied by a power of 10, and there are 10 digits \(0-9\). So if we have a number such as 457, it can be represented as the following: $$4*(10^2) + 5*(10^1) + 7*(10^0)$$. If you don't know what an exponent is, that's ok too, you can basically interpret the previous expression as the following: $$$$$$4*(10*10) + 5*(10) + 7*(1)$$.

In base-2, we have each digit be multiplied by a power of 2, and there are only 2 digits. Lets look into how we convert a number such as 19 to binary. 19 in base-10 is represented as the following: $$1*(10^1) + 9*(10^0)$$. Lets see how we'd represent this in base-2. In base 2, the powers of 2 are the following: $$1, 2, 4, 8, 16, 32, 64, ...$$ . So in order to have a number in base-2, it would be represented as 1s and 0s multiplied by powers of 2.

This table might come in handy:

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 0 | 1 | 0 | 0 | 1 | 1 |

We want to convert 19 to binary, so in order to do this we find the biggest power of 2 which can fit into 19. In this case, it's 16. Lets put a 1 at the 16 spot in the table. so now our binary representation \(which is incomplete\), is `00010000`. Now we subtract 16 from 19, and repeat this process until we remain with 0. We have 3, and the highest power we can pack into that is 2. Now we subtract 2 from 3, and place a 1 in the 2 spot in the table. Our binary representation is now: `00010010`.Now we are left with 1, and we'll place a 1 in the 1 spot in the table. We are left with 0, and our binary representation is the following: `00010011`.

### Exercises:

1. What is 75 in binary?
2. What is 13 in binary?
3. What is 36 in binary?
4. What is 10010101 in decimal?
5. What is 11010001 in decimal?
6. What is 00101001 in decimal?

> "signed"

What does it mean for a data type \(in almost all cases a numeric data type\) to be signed? If an integer is stored in 32 bits, lets use our old example above: `11000010011011010110110111011111`.

Lets concentrate our focus to integers, since we will only be dealing with integers in this section. A signed integer is an integer where the first bit decides the sign of the integer. In our integer above, our bits start off like this: `11000...` The first bit is set to 1, so we know that this is a negative number. The other 31 bits then decide what the number actually is. 

