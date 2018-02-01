# Strings

In java, Strings are a sequence of characters. You might have noticed that in Java, a string is not a primitive data type,  and is initialized using the `String` class. You'll also notice that in the rules,  you must know the following methods: `length, charAt, getChars, equals, equalsIgnoreCase, startsWith, endsWith, indexOf, lastIndexOf, substring, and concat`. You will also need to know string concatenation using the `+`  operator. I will be going over each method in detail.

Before I go into the methods, let's briefly look into how to instantiate a string:

```
String a = "this is a string";                    // "this is a string"
String b = new String("this is another string");  // "this is another string"
char[] c = {'s', 't', 'r', 'i', 'n', 'g', 's'};
String d = new String(c);                         // "strings"
```

As you can see, there are multiple ways to instantiate a string; you can even use a character array.

### length

This method is very self explanatory. You basically get the length of a string. Let's see it's usage below:

```
String a = "a string";
int a_length = a.length(); // 8

String b = "";
int b_length = b.length(); // 0
```

#### Exercises

1. What is the result of `"hello world".length()` ?
2. What is the result of `"this is a str".length()` ?
3. What is the result of `"coding".length()` ?

### charAt

This method gets the character at a certain index of a string. Let's see it's usage below:

```
String a = "a string";
char b   = a.charAt(0); // 'a'
char c   = a.charAt(6); // 'n'
```

Note that this method doesn't work at all on an empty string.

#### Exercises

1. What is the result of `"hello world".charAt(6)` ?
2. What is the result of `"this is a str".charAt(11)` ?
3. What is the result of `"coding".charAt(3)` ?

### getChars

This method is a bit more complicated. The syntax of this method is below:

```
public void getChars(int srcBegin, int srcEnd, char[] dst,  int dstBegin)
```

`srcBegin` is the index of the first character in the string to copy

`srcEnd` is the index after the last character in the string to copy

`dst` is the character array you copy the characters to, aka the destination array

`dstBegin` is the start offset in the destination array \(i.e. the index where you begin copying the characters\)

This method is probably one of the most confusing methods to figure out, so I'll go through some examples to make things clear.

```
String str1 = "Code Analysis!";
char[] str2 = new char[8];

str1.getChars(5,13,str2,0);
```

This table should explain how str1 is structured:

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| C | o | d | e |  | A | n | a | l | y | s | i | s | ! |

As you can see in the code block, we use `getChars` on str1, and our starting index is `5` , so we INCLUDE the `A` character, and our ending index is `13` , but we EXCLUDE the `!` character, so our full string that we extract becomes `"Analysis"` .  Our source character array is also of length 8 \(by the way make sure your destination array can fit the string you extract\). We set our offset to `0` , because we want to start copying characters from the beginning of the array. Thus, the character array now looks like this:

```
str2 = {'A', 'n', 'a', 'l', 'y', 's', 'i', 's'};
```

#### Exercises

For these exercises, I will give them in code blocks

```
// 1.
String str1 = "Code Analysis!";
char[] str2 = new char[4];

str1.getChars(0,4,str2,0);

// What is the value of str2: {_, _, _, _} ?
```

```
// 2.
String str1 = "Does anyone remember CodeBusters 2014?";
char[] str2 = new char[8];

str1.getChars(21,25,str2,0);

// What is the value of str2: {_, _, _, _, _, _, _, _} ?
```

```
// 3.
String str1 = "The States test will be really hard";
char[] str2 = new char[8];

str1.getChars(11,15,str2,4);

// What is the value of str2: {_, _, _, _, _, _, _, _} ?
```

### equals

This method checks if two strings are equal. Let's see it's usage below:

```
String a = "this";
String b = "that";
String c = "this";

boolean d = a.equals(b); // false
boolean e = a.equals(c); // true
```

#### Exercises

1. What is the result of `"hey".equals("hello")` ?
2. What is the result of `"what".equals("what")` ?
3. What is the result of `"this is tedious".equals("This is tedious")`?

### equalsIgnoresCase

This method checks if two strings are equal, BUT it ignores case. Let's see it's usage below:

```
String a = "this";
String b = "This";
String c = "THIS";
String d = "that";

boolean e = a.equals(b); // true
boolean f = a.equals(c); // true
```

#### Exercises

1. What is the result of `"what".equals("whAt")` ?
2. What is the result of `"this".equals("th1s")` ?
3. What is the result of `"whoa".equals("WHOA")` ?

### startsWith

This method actually has two ways of being used: `boolean startsWith(String str)`, and `boolean startsWith(String str, index fromIndex)`. The first way simply checks if a string starts with `str`, and the second way checks if a string starts with `str` _from a specified index in the original string_. 











