# Operator Precedence and Associativity

### Operator Prededence

In Java, all operators have some level of priority, which the program must obey when the program is being executed. This concept is similar to PEMDAS in regular math, but with a bit more complexity for programming. The table below highlights which operators have priority over which other operators.

![](/assets/operator_precedence.png)

In order to read this table, consider the top of the table, level 16, as operators that are considered first before anything. If you ever get confused, notice how there are parentheses in that level, which is the first letter in PEMDAS, and that should help you orient yourself. I know that you don't have to all these operators, but for the ones you are required to know, note their place in this table.

#### Exercises

1. What is the result of `2 + 3 * 5` ?
2. What is the result of `5 & 6 > 7` ?
3. What is the result of `3 & 4 ^ 5` ?
4. What is the result of `2 + 3 ^ 5 | 8` ?
5. What is the result of `true || false && !false` ?
6. What is the result of `(true || false) && true` ?

### Operator Associativity

In order to understand operator precedence completely, we must understand operator associativity as well. Operator associativity is a property that determines how operators of the same precedence are grouped in the absence of parentheses.  



