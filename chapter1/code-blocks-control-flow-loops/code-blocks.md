# Blocks

A "regular" block of code contains all the variables instantiated inside the block inside it's "scope." Let me explain what that means through an example:

```
class Main {
    public static void main(String[] args) {

        {
            int a = 7;
            a++;
            System.out.println(a);
        }

        System.out.println(a);
    }
}
```

Note that this code **won't compile**. This is because it'll find the `a` and see that it hasn't been instantiated in that scope. You might think "oh wait but it's inside that code block!" Yes, it is, but as soon as the block ends, the `a` variable in that block is deleted. This leaves there being no `a` variable in the parent scope, which the compiler recognizes and breaks when you try to compile it.

