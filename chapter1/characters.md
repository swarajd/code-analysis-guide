# Characters

In java, the primitive `char` type stores single characters. Note: please do NOT include an ascii table on your cheat sheet as we will provide that for you. Let's look at an example of a character in java:

```
char someChar = 'a';
char someOtherChar = '~';
```

### Character range

According to the rules, we will only be dealing with the characters from `' '` to `'~'` \(space to tilde\). In order to understand what this really means, lets look at an ascii table:

![](/assets/asciitable.png)\(source: [https://commons.wikimedia.org/wiki/File:ASCII-Table-wide.svg\](https://commons.wikimedia.org/wiki/File:ASCII-Table-wide.svg\)\)

From this table, we can see that we only deal with the characters from `32` to `126` . You might have also noticed that characters correspond to decimal and hexadecimal values. That means that in java you can do something like this: 

```
char a = (char)32;         // the ' ' character (space)
char b = (char)76;         // the 'L' character 
char c = (char)0x4D;       // the 'M' character
char d = (char)0101;       // the 'A' character
char e = (char)0b1001111;  // the 'O' character
```

### Escape Sequences

The rules also mention that we can use the following escape sequences: `\\, \', \"` . Lets look at how these are parsed in java:

```
char backslash = '\\';  // This will be printed like this: \
char singquote = '\'';  // This will be printed like this: '
char doubquote = '\"';  // This will be printed like this: "
```

### Character arithmetic





