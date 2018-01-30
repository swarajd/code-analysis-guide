# Representations

According to the rules, you should be able to read binary, octal, and hexadecimal constants, so this section will cover how to read those three formats for numbers. We have already been over binary, so this section will focus on octal and hexadecimal.

### Octal

As a review, if we want to write a number in base-10, we write it as multiplications of powers of 10, using the 10 digits \(0-9\). So if we have a number such as 457, it can be represented as the following: $$4*(10^2) + 5*(10^1) + 7*(10^0)$$. If you don't know what an exponent is, that's ok too, you can basically interpret the previous expression as the following:$$4*(10*10) + 5*(10) + 7*(1)$$.

In base-8, or octal, we have each digit be multiplied by a power of 8, and there are only 8 digits \(0-7\). Lets look into how we convert a number such as 19 into octal. 19 in base-10 is represented as the following: $$1*(10^1) + 9*(10^0)$$. Let's see how we'd represent this in base-8. In base-8, the powers of 8 are the following: $$1, 8, 64, 512, 4096, ...$$. So in order to have a number in base-8, it would be represented as the digits 0-7 by powers of 8.

This table might come in handy:

| 4096 | 512 | 64 | 8 | 1 |
| :--- | :--- | :--- | :--- | :--- |
| 0 | 0 | 0 | 2 | 3 |

We want to convert 19 to octal, so in order to do this we find the biggest power of 8 which can fit into 19. In this case, it's 8. Lets put a 2 at the 8 spot in the table. So now we subtract $$8 * 2 = 16$$ from 19, and we're left with 3. Our octal representation is now `00020`. Now we repeat this process until we remain with 0. We have 3, and the highest power we can pack into that is $$1 * 3 = 3$$. Now we subtract 3 from 3, and place a 3 in the 1 spot in the table. Our octal representation is now: `00023`.Now we are left with 0, so our octal representation is complete as `00023`.

### Exercises:

1. What is 75 in octal?
2. What is 13 in octal?
3. What is 36 in octal?
4. What is 75 \(currently octal\) in decimal?
5. What is 13 \(currently octal\) in decimal?
6. What is 36 \(currently octal\) in decimal?

### Hexadecimal

In base-16, or hexadecimal, we have each digit be multiplied by a power of 16, and there are actually 15 digits: `0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F`. If you want, you can think of `A` as being equal to $$ 10$$, `B` being equal to $$ 11$$, and so on.

We already know how 19 is represented 

