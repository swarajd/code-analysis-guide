# Boolean Values

In Java, a Boolean value is one with two choices: true or false, yes or no, 1 or 0. Lets look at a few examples of booleans below:

```
boolean a = true;
boolean b = false;
```

Pretty simple, right? There are only two values for booleans, and they're `true` and `false` . However, there's a lot more to booleans than just these two values. There are a number of operators that can be applied to boolean values, which I'll explain below. 

### Boolean Unary Operators

Just like there is one unary operator for integers, there is one unary operator for boolean values: `!`. This operator basically flips the value of the boolean. 

```
boolean a = true;
boolean b = false;
boolean c = !a;    // false
boolean d = !b;    // true
```

### Boolean Binary Operators

There are 9 different binary operators for booleans: `==, !=, <, <=, >, >=, &&, ||, ^` . I will explain what they do below:

`==` : This operator checks if two boolean values are equal. Let's see how it works in the table below

| a | b | a == b |
| :--- | :--- | :--- |
| false | false | true |
| false | true | false |
| true | false | false |
| true | true | true |

`!=` : This operator is literally the opposite of the above operator. Let's look at the table below to see how it works:

| a | b | a != b |
| :--- | :--- | :--- |
| false | false | false |
| false | true | true |
| true | false | true |
| true | true | false |

`<` : This operator checks if the previous integer \(or any numeric type\) is _strictly less than_ the integer after the operator. Lets check out a few examples:

```
boolean a = 2 < 3; // true
boolean b = 3 < 2; // false
boolean c = 3 < 3; // false
```

`<=` : This operator checks for _less than or equal to_. Lets check out a few examples:

```
boolean a = 2 <= 3; // true
boolean b = 3 <= 2; // false
boolean c = 3 <= 3; // true
```

Notice how the third boolean equates to true, because 3 **is** less than or equal to 3.

I won't be going over the `>` and `>=` operators \(_greater than_ and _greater than or equal to_\), as they're self explanatory really. 

`&&` : This operator takes two boolean values and checks if both of them are true. Let's look at the table below to see how it works:

| a | b | a && b |
| :--- | :--- | :--- |
| false | false | false |
| false | true | false |
| true | false | false |
| true | true | true |

Notice how this operator is similar to the bitwise and back in the binary operators for integers. That's because you can think of `true` and `false` as bits. 

`||` : This operator is basically the same as bitwise OR, lets see how below:

| a | b | a \|\| b |
| :--- | :--- | :--- |
| false | false | false |
| false | true | true |
| true | false | true |
| true | true | true |

`^` : This operator is basically the same as bitwise XOR. See below:

| a | b | a ^ b |
| :--- | :--- | :--- |
| false | false | false |
| false | true | true |
| true | false | true |
| true | true | false |

Note: this seems like it's equivalent to `!=` , but for boolean values I would use `!=` as it's much clearer.

