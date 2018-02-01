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

### charAt

This method gets the character at a certain index of a string. Let's see it's usage below:

```
String a = "a string";
char b   = a.charAt(0); // 'a'
char c   = a.charAt(6); // 'n'
```

Note that this method doesn't work at all on an empty string.

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



