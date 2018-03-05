# Operator Precedence and Associativity

### Operator Prededence

In Java, all operators have some level of priority, which the program must obey when the program is being executed. This concept is similar to PEMDAS in regular math, but with a bit more complexity for programming. The table below highlights which operators have priority over which other operators.

![](/assets/operator_precedence.png)

In order to read this table, consider the top of the table, level 16, as operators that are considered first before anything. If you ever get confused, notice how there are parentheses in that level, which is the first letter in PEMDAS, and that should help you orient yourself. I know that you don't have to know all these operators, but for the ones you are required to know, note their place in this table.

#### Exercises

1. What is the result of `2 + 3 * 5` ?
2. What is the result of `5 & 6 > 7` ?
3. What is the result of `3 & 4 ^ 5` ?
4. What is the result of `2 + 3 ^ 5 | 8` ?
5. What is the result of `true || false && !false` ?
6. What is the result of `(true || false) && true` ?

### Operator Associativity

In order to understand operator precedence completely, we must understand operator associativity as well. Operator associativity is a property that determines how operators of the same precedence are grouped in the absence of parentheses.

Lets see this in practice:

```
int a = 3 + 4 - 5;
a     = 7 - 5;
a     = 2;
```

All of these expressions are the same, but the way they're resolved is from left to right \(according to the table above\), so you would first resolve the `+`, then the `-` .

However, not all operators are like this. If you view the table above, there are some operators that have associativity from right to left. One such example of this is the ternary operator. Let's see this in practice:

```
int a = true ? true ? 2 : 3 : 4;
a     = true ? 2 : 4;
a     = 2;
```

In this case, the ternary operator "inside" the ternary operator is resolved first, so in this case you'd resolve it "inside-out," which is basically "right-to-left."

#### Exercises

1. What is the result of `1 + 2 + 3 - 4` ?
2. What is the result of `11235 >> 2 >> 3 >> 4` ?
3. What is the result of `7 & 12 & 5` ?
4. What is the result of `3 ^ 4 ^ 3` ?
5. What is the result of `true == false == true == false` ?
6. What is the result of `11235 >> 2 >> (3 >> 4)`?



