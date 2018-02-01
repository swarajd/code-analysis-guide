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

Arrays don't necessarily have to have 1 dimension, either. You can create a 2-dimensional array as such:

```
int[][] twodim = new int[3][4]; // this array has 3 'rows' and 4 'columns'
/*
    the above array is structures like this:

    {
        {0, 0, 0, 0},
        {0, 0, 0, 0}
        {0, 0, 0, 0}
    }

    Notice how this is an array of arrays. There are 3 arrays of length 4, hence "new int[3][4]"
    To remember it easier, think of it like "new int[rows][cols]"
*/
```

We can also edit and access the contents of a two-dimensional array as well. Lets look at a few examples of these, continuing from the two-dimensional array we have above.

```
twodim[2][3] = 6;
twodim[1][2] = 4;
twodim[0][0] = twodim[2][3] + twodim[1][2]; // 10

int a = twodim[0][0]; // 10
```

### Exercises

For this section of exercises, I will provide a code block for each, and you will fill in the correct value.

```
// 1.
int[] arr = new int[10];
arr[0] = 7;
arr[3] = 8;
arr[5] = 9;
arr[2] = arr[3] + arr[5];
arr[4] = arr[0] + arr[3];
arr[6] = arr[2] + arr[4];

int a = arr[6]; //What is the variable 'a' equal to: ___ ?
```

```
// 2. 
// set the 5th value of the array to 7

int[] arr = new int[10];

arr[___] = 7;
```

```
// 3.
int[][] arr = new int[3][3];
arr[0][0] = 1;
arr[1][1] = 1;
arr[2][0] = 1;
arr[0][2] = 1;
arr[2][2] = 1;

// fill out the values of the array below:
{
    {__, __, __},
    {__, __, __},
    {__, __, __}
}
```



