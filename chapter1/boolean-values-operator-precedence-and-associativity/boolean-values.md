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

Note: this seems like it's equivalent to `!=` , but for boolean values you should use `!=` as it's much clearer. However, be prepared for either use in the actual event.

#### Exercises

1. What is the result of `true == false` ?
2. What is the result of `false != false` ?
3. What is the result of `false || true` ?
4. What is the result of `true ^ false` ?
5. What is the result of `false && false` ?
6. What is the result of `9 >= 8` ?
7. What is the result of `2 < 5` ?
8. What is the result of `7 <= 7` ?
9. What is the result of `8 > 4` ?

### Boolean Ternary Operators

If you don't know what a ternary operator is, it is an operator that takes three values and produces one result. In java, the only ternary operator for boolean values is in the format `a ? b : c` .  The way this works is if `a` is true, then the operator will return `b`, otherwise it'll return `c` . Keep in mind that the values `b` and `c` don't necessarily have to be boolean values and the purpose of ternary operators is to choose between two values of the same type. Lets look at a few values below:

```
int a = true ? 1 : 2;             // 1
char b = false ? 'x' : 'y';       // 'y'
boolean c = false ? true : false; // false;
```

#### Exercises

1. What is the result of `true ? 7 : 6` ?
2. What is the result of `false ? 'a' : 'b'` ?
3. What is the result of `false ? false : true` ?
4. What is the result of `true ? false : true` ?
5. What is the result of `false ? 0 : 1` ?
6. What is the result of `true ? 35 : 53` ?





