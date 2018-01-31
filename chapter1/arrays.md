# Arrays

An array in java is a group of like-typed variables that are referred to by a common name. Arrays in java are structured as such:

Lets say this array is called `arr`, and this array is of length 5. 

| 0 | 1 | 2 | 3 | 4 |
| :--- | :--- | :--- | :--- | :--- |
| first elem, arr\[0\] |  |  |  | fifth elem, arr\[4\] |



Let's look at an example of an array in java:

```
int[] arr_a = new int[5];                       // this is the array: {0, 0, 0, 0, 0}
char[] arr_b = {'c', 'o', 'd', 'i', 'n', 'g'};  // this is the array: {'c', 'o', 'd', 'i', 'n', 'g'}
boolean[] arr_c = new boolean[2];               // this is the array: {false, false}
```

In addition to initializing arrays, you can also edit and access the contents of the array as well. Lets look at a few examples of these, continuing on from the arrays we have above. 

```
int a  = arr_a[3];   // 0
char b = arr_b[5];   // 'g'

arr_a[4] = 7;        // arr_a = {0, 0, 0, 0, 7}
arr_c[0] = true;     // arr_c = {true, false}

boolean c = arr_c[0] // true
int d     = arr_a[4] // 7
```



