# Unary Operators

There is only one unary operator, and that is `-` . This operator turns an integer into it's negative \(or positive\) counterpart. 

One edge case I will go over, however, is the use of this operator on the smallest integer. As you should know from the previous section, the smallest representable integer in 32 bits is $$ -2147483648$$. So what happens if we do the following:

```
int a = -2147483648;
int b = -a;
```

Now I didn't really go over this in the previous section, but to go from a negative number to a positive number, you basically follow the same procedure, so if we have $$-109$$, which is represented as such: `10010011`. We can then flip the bits, getting us `01101100`, and add 1, getting us `01101101`, which gets us back $$109$$.

In the code block above, we have the smallest integer value, which is represented as such `10000000000000000000000000000000`. Lets try and switch the sign of this. First we flip all the bits: `01111111111111111111111111111111`. Now, when we add 1 to this, we will get back our original binary, which is `10000000000000000000000000000000` .

Keep in mind this edge case, as it's often something that programmers overlook.

### 



