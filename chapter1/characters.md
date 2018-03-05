# Characters

In java, the primitive `char` type stores single characters. Note: please do NOT include an ascii table on your cheat sheet as we will provide that for you. Let's look at an example of a character in java:

```
char someChar = 'a';
char someOtherChar = '~';
```

### Character range

According to the rules, we will only be dealing with the characters from `' '` to `'~'` \(space to tilde\). In order to understand what this really means, lets look at an ascii table:

![](/assets/asciitable.png)\(source: [https://commons.wikimedia.org/wiki/File:ASCII-Table-wide.svg\](https://commons.wikimedia.org/wiki/File:ASCII-Table-wide.svg%29\)\)

sFrom this table, we can see that we only deal with the characters from `32` to `126` . You might have also noticed that characters correspond to decimal and hexadecimal values. That means that in java you can do something like this:

```
char a = (char)32;         // the ' ' character (space)
char b = (char)76;         // the 'L' character 
char c = (char)0x4D;       // the 'M' character
char d = (char)0101;       // the 'A' character
char e = (char)0b1001111;  // the 'O' characte
```

#### Exercises

1. What character is represented by the decimal value `40` ?
2. What character is represented by the octal value `40`?
3. What character is represented by the hexadecimal value `40` ?
4. What is `'T'` in decimal?
5. What is `'O'` in octal?
6. What is `'P'` in hexadecimal?

### Escape Sequences

The rules also mention that we can use the following escape sequences: `\\, \', \"` . Lets look at how these are parsed in java:

```
char backslash = '\\';  // This will be printed like this: \
char singquote = '\'';  // This will be printed like this: '
char doubquote = '\"';  // This will be printed like this: "
```

#### Exercises

1. How is `"I am a coo\\ dude"`  printed?
2. How is `"This is a \"great\" guide"` printed?
3. How is `"It\'s or It is?"` printed?
4. How is `"\\33tc0d3"` printed?
5. How is `"\"\""` printed?
6. How is `"\'\'\'"` printed?

### Character arithmetic

The rules also say you can perform character arithmetic, but only if the result is in the range from `'0'` to `'9'` , or from `'A'` to `'Z'` , or from `'a'` to `'z'` .  Lets look into some examples of character arithmetic:

    char cd    = 'c' + 'd' - '`'; // The resulting character is 'g'
    char char7 = '3' + '4' - '0'; // The resulting character is '7'
    char CD    = 'C' + 'D' - '@'; // The resulting character is 'G'

The way this arithmetic works is `char` s are basically 8 bit integers, and it does the arithmetic on the integer values and 'converts' it back to a character.

#### Exercises

1. What is `(char)('7' * 2)` ?
2. What is `(char)(0x20 + 77)` ?
3. What is `(char)('6' + 'C')` ?
4. What is `(char)('z' - '\"')` ?
5. What is `(char)('d' - '1')` ?
6. What is `(char)('!' + '!' + '\"')` ?



