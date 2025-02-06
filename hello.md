# C Language Questions

---

Here are some interview level questions and answers

### Q 1. How to reverse an array in C.

It is a swapping technique.
where

- n = length of Array
- start = starting index of array
- temp = It is a temporary variable

```bash
    int main(){
    int *arr,n;

    scanf("%d",&n);
    arr = (int *) malloc(n*sizeof(int));

    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }

    int start=0,end=n-1,temp;

    while(start<end){
        temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        start++;
        end--;
    }
    return 0;
    }

```

### Q 2. How find (extract) words from an array of string or sentence.

```bash

int main() {

    char *s;
    s = malloc(1024 * sizeof(char));

    scanf("%[^\n]", s);
    s = realloc(s, strlen(s) + 1);

    int i=0,flag=0;

    while(s[i] != '\0'){
    if (s[i] == ' ' || s[i] == '\n') {
            if (flag) {
                printf("\n");
                flag = 0;
            }
        } else {
            printf("%c", s[i]);
            flag = 1;
        }
    i++;
    }

    return 0;
}

```

### Q 3. Given a string, consisting of alphabets and digits, find the frequency of each digit in the given string.

```bash

    int main() {
        char *str;
        int i=0,freq[10]={0};

        str = malloc(1024 * sizeof(char));
        scanf("%[^\n]",str);

        str = realloc(str, strlen(str)+1);

        while (str[i] != '\0') {
            if(str[i] >= '0' && str[i] <= '9'){
            freq[str[i] - '0']++;
            }
        i++;
        }

        for(int i=0;i<10;i++){
            printf("%d ",freq[i]);
        }

    return 0;
}


```

---

---

---

### Question 1

**What function do we use to print text to standard output in C ? [See Answer](#answer1)**

- console.log()
- printf()
- scanf()
- cout<<

### Question 2

**What will be the output of the code snippet? ? [See Answer](#answer)**

```bash
#include <stdio.h>
int main() {
    printf("%d", 5 / 2);
    return 0;
}
```

- 2.0
- 2.5
- 2
- 3

### Question 3

**What will be the output of the code snippet? ? [See Answer](#answer)**

```bash
#include <stdio.h>
int main() {
    printf("Hello, ");
    printf("world!");
    return 0;
}
```

- Hello, world!
- Hello <br>
  world!
- HelloWorld!
- Hello world!

### Question 4

**How do you print the number 108 using arithmetic operations on the numbers 9 and 12 in C ? [See Answer](#answer)**

- print(9/12);
- print(9\*12);
- cout<<9\*12;
- printf("%d", 9\*12);

### Question 5

**How can we print the difference between 9 and 3 in C ? [See Answer](#answer)**

- print(9-3);
- cout<<9-3;
- printf("%d", 9-3);
- printf("%d", 9)-printf("%d", 3);

### Question 6

**What will be the output of the code snippet? [See Answer](#answer)**

```bash
#include <stdio.h>
int main() {
    printf("%d ",10/2);
    printf("%d", 10/2.00 + 1);
    return 0;
}
```

- 5 6
- 5 5
- 5 Undefined Value
- 6 5

### Question 7

**How to print the digit '9' as a character in C? [See Answer](#answer)**

- printf("%c", '9');
- printf("%a", '9');
- printf("%d", '9');
- printf("%s", '9');

### Question 8

**What will be the output of this code snippet? [See Answer](#answer)**

```bash
#include <stdio.h>
int main() {
    printf("%d", 10 % 3);
    return 0;
}
```

- 1
- 2
- 3
- 00

### Question 9

**What would be the output of the following code: [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("Hello\nAnd Welcome John");
}
```

- HelloAnd Welcome John
- Hello <br>
  And Welcome John
- Hello And <br>
  Welcome John
- Hello <br>
  And Welcome <br>
  John

### Question 10

**What would be the output of the following code: [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    char ch = 'A';
    printf("%c", ch + 1);
    return 0;
}
```

- A
- B
- 66
- Compilation Error

### Question 11

**What would be the output of the following code: [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("%f", 10);
    return 0;
}
```

- 10.0
- 10
- Undefined
- Compilation Error

### Question 12

**Write a C program to find the sum of two numbers, 4 and 8. [See Answer](#answer)**

### Question 13

**Write a C program to print $ [See Answer](#answer)**

### Question 14

**What will the following C code print? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("Hello ");
    printf("World!");

    return 0;
}
```

- Hello World!
- Hello\nWorld!
- Hello
- World!

### Question 15

**Which of these statements prints the displayed text in the problem statement? [See Answer](#answer)**

<pre>
Hello
World!
</pre>

- printf("Hello World!");
- printf("Hello"); printf("World!");
- printf("Hello\nWorld!");
- printf("Hello"); \n printf("World!");

### Question 16

**What is the output of the given code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("1 + 2 = %d", 1 + 2);
    return 0;
}
```

- 1 + 2 = 3
- 1 + 2
- 3
- 6

### Question 17

**What will be printed by the given code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("Prints %s and %s", "on", "multiple lines");
    return 0;
}
```

- Prints on and multiple lines
- Prints on multiple lines
- Prints %s and %s
- Error

### Question 18

**What will be the output of the given code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("Programming");
    printf("Language");
}
```

- Programming\nLanguage
- ProgrammingLanguage
- Programming<br>
  Language
- Programming <br>
  Lanugage

### Question 19

**What will be the output of this C code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("1\n2\n3");
    return 0;
}
```

- 1\n2 <br>
  3
- 1\n2\n3
- 123
- 1<br>
  2<br>
  3

### Question 20

**What will be printed by the given C code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("This is a backslash: \\");
    return 0;
}
```

- This is a backslash: \
- This is a backslash: \\
- This is a backslash:
- This is a backslash: \n

### Question 21

**What will be the output of the given code snippet? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("Hello, ");
    printf("how are you?\n");
    printf("I'm fine.");
    return 0;
}
```

- Hello, how are you?
- Hello, how are you?<br>
  I'm fine.
- Hello, <br>
  how are you? <br>
  I'm fine.

### Question 22

**Write a C program to print the following output using a single printf statement: [See Answer](#answer)**

```bash
The result of 5 + 3 is:
8
```

-
-
-
-

### Question 23

**Write a C program to print the following pattern using a single printf statement: [See Answer](#answer)**

```bash
      *
    * * *
  * * * * *
* * * * * * *
```

### Question 24

**What would be the output of the following code: [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
   printf("In the\nmiddle of difficulty\nlies opportunity");
}
```

- In the middle of difficulty<br>
  lies opportunity
- In the<br>
  middle of difficulty lies opportunity
- In the<br>
  middle of difficulty<br>
  lies opportunity
- In the middle of difficulty lies opportunity

### Question 25

**What would be the output of the following code: [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
   printf("1\n1 2\n1 2 3\n1 2 3 4");
}
```

- 1 1 2 1 2 3<br>
  1 2 3 4
- 1 <br>
  1 2 1 2 3<br>
  1 2 3 4
- 1 1 2 1 2 3 1 2 3 4
- 1 <br>
  1 2<br>
  1 2 3<br>
  1 2 3 4

### Question 26

**What would be the output of the following code: [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
   printf("    *\n   **\n  ***\n ****\n*****");
}
```

- <pre>  
      *
      * * 
      * * * 
      * * * * 
      * * * * *
  </pre>

- <pre>  
              *
            * * 
          * * * 
        * * * * 
      * * * * *
  </pre>

- <pre>
            *
          * * *
        * * * * *
      * * * * * * *
  </pre>

- <pre>
      *  **  ***  ****  *****
  </pre>

### Question 27

**What does this C code print? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    int number = 10;
    printf("%d", number);
    return 0;
}
```

- 10
- number
- 00
- Error



### Question 28

**What is the output of the given C code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    float value = 7.8;
    printf("%f", value);
    return 0;
}
```

- 7
- 7.800000
- 8
- 7.5

### Question 29

**What does this C code print? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    char letter;
    letter = 'A';
    printf("%c", letter);
    return 0;
}
```

- A
- letter
- 65
- 1

### Question 30

**What is the output of the following C code?
(Consider the modern 32-bit computer architecture [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    printf("Size of double: %lu", sizeof(double));
    return 0;
}
```

- Size of double: 4
- Size of double: 8
- Size of double: 2
- Error

### Question 31

**What does the given C code print? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    int num = 5;
    {
        int num = 10;
        printf("%d ", num);
    }
    printf("%d", num);
    return 0;
}
```

- 10 5
- 5 10
- 10 10
- Error

### Question 32

**What is the output of the following C code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    int integer = 5;
    float floating = 7.2;
    printf("%f", integer + floating);
    return 0;
}
```

- 12.200000
- 5.0
- 7
- 7.00

### Question 33

**What does this C code print? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    int x = 2, y = 3, z;
    z = x * y;
    printf("%d", z);
    return 0;
}
```

- 5
- x \* y
- 6
- 3 \* 2

### Question 34

**What is the output of the following C code? [See Answer](#answer)**

```bash
#include <stdio.h>

int main() {
    char character = 130;
    printf("%d", character);
    return 0;
}
```

- 140
- 126
- 256
- 130

### Question 35

**Which of the following is NOT a valid data type in C? [See Answer](#answer)**

- float
- char
- string
- double

### Question 36

**What will be the output of the following code snippet? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    float num = 10 / 3;
    printf("%f\n", num);
    return 0;
}
```
- 3.333333
- 3.000000
- 3
- Compilation Error

### Question 37

**Write a C program that swaps the values of two integer variables, a =5 and b = 10, and prints their new values using a single printf statement with a space between them [See Answer](#answer)**


### Question 38

**Write a C program that converts a temperature in Celsius to Fahrenheit. The Celsius temperature should be stored in a float variable celsius, and the Fahrenheit equivalent should be printed using a single printf statement. The relation between the two scales is given as <br>
fahrenheit = (celsius * 9/5) + 32; <br>
Take the celsius temperature to be 20.5. [See Answer](#answer)**

### Question 39

**Now do the reverse, write a C program that converts a temperature in Fahrenheit to Celsius. The Fahrenheit temperature should be stored in a float variable fahrenheit, and the Celsius equivalent should be printed using a single printf statement.<br>
We can use the same relation between the two scales:<br>
fahrenheit = (celsius * 9/5) + 32;
Take the Fahrenheit temperature to be 98.3. [See Answer](#answer)**


### Question 40

**Given the height (1.82 meter) and weight (72 kg) of the Chef, calculate his BMI (Body Mass Index).<br>
Formula to calculate the BMI: [See Answer](#answer)**

![This is formula for BMI](https://cdn.codechef.com/images/learning/bmi_formula.png)


### Question 41

**What would be the output of the following code: [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    int x = 5;
    float f = 3.4;
    printf("%d\n%d", x, f);
}
```
- 5 3.4
- 5 <br>
3.4
- Compilation Error
- 5<br>
random number


### Question 42

**What will the following code ? [See Answer](#answer)**
```bash
#include <stdio.h>
int main() {
    char a[1],b[1];
    int c;
    scanf("%d", &a);
    scanf("%d", &b);
    c = a + b;
    printf("%d", c);
    return 0;
}
```
- The code will lead to a compilation error.
- 2
- undefined

### Question 43

**What would be the output of the given code if the user enters the temperature 25? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    int temperature;
    printf("Enter the temperature in Celsius: ");
    scanf("%d", &temperature);

    if (temperature < 0) {
        printf("It's freezing cold!");
    } else if (temperature >= 0 && temperature <= 20) {
        printf("It's a bit chilly.");
    } else if (temperature > 20 && temperature <= 30) {
        printf("It's a pleasant day.");
    } else {
        printf("It's quite warm!");
    }

    return 0;
}
```

- It's freezing cold!
- It's a bit chilly.
- It's a pleasant day.
- It's quite warm!

### Question 44

**What is the purpose of the if/else construct in the given code ? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    int num1, num2;
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    if (num1 > num2) {
        printf("%d is the largest number.\n", num1);
    } else {
        printf("%d is the largest number.\n", num2);
    }

    return 0;
}
```
- Find the sum of two numbers
- Check if the numbers are equal
- Find the smallest number
- Find the largest number


### Question 45

**What would be the output of the given code if the user enters the signal as 'Y'? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    char signal;
    printf("Enter the traffic light signal (R/Y/G): ");
    scanf(" %c", &signal);

    if (signal == 'R') {
        printf("Stop! It's red signal.");
    } else if (signal == 'Y') {
        printf("Get ready to move. It's yellow signal.");
    } else if (signal == 'G') {
        printf("Go! It's green signal.");
    } else {
        printf("Invalid signal input.");
    }

    return 0;
}
```
- Stop! It's red signal.
- Get ready to move. It's yellow signal.
- Go! It's green signal.
- Invalid signal input.


### Question 46

**What would be the output of the given code if the user enters the day number 3? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    int day;
    printf("Enter a day number (1-7): ");
    scanf("%d", &day);

    if (day >= 1) {
        if (day == 1) {
            printf("It's Monday!");
        } else if (day == 2) {
            printf("It's Wednesday!");
        } else if (day == 3) {
            printf("It's Friday!");
        } else if (day == 4) {
            printf("It's Sunday!");
        } else {
            printf("Invalid day number.");
        }
    } else {
        printf("Invalid day number.");
    }

    return 0;
}
```
- It's Monday!
- It's Wednesday!
- It's Friday!
- It's Sunday!


### Question 47

**What is the purpose of the if/else if/else construct in the given code ? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    int age;
    printf("Enter your age: ");
    scanf("%d", &age);

    if (age < 18) {
        printf("You are in the child age group.\n");
    } else if (age < 60) {
        printf("You are in the adult age group.\n");
    } else {
        printf("You are in the senior age group.\n");
    }

    return 0;
}
```
- Check if the age is less than 10
- Identify the age group as child, adult, or senior
- Check if the age is a multiple of 5
- Check if the age is greater than 100


### Question 48

**Write a C program that takes three integers as input and determines the largest among them. Print the largest number. [See Answer](#answer)**


### Question 49

**Given two space separated integers as user inputs, print YES if their sum is even else NO. [See Answer](#answer49)**


### Question 50

**Take the sides of a triangle as user inputs and find if the triangle is equilateral, isosceles, or scalene.**

#### Note:
Equilateral Triangle: If all three sides of the triangle are equal, it is an equilateral triangle.
Isosceles Triangle: If at least two sides of the triangle are equal, it is an isosceles triangle.
Scalene Triangle: If all three sides of the triangle are different, it is a scalene triangle.

#### Input Format
The only line of input will contain three space separated numbers - The sides of a triangle.
Output Format
Output on a single line:
Equilateral, if the triangle is equilateral.
Isosceles, if the triangle is isosceles.
Scalene, if the triangle is scalene. [See Answer](#answer50)



### Question 51

**In C, what statement do you use to check whether a variable A 
A is equal to 2?
And if it is, print 9. [See Answer](#answer51)**

- Option 1
```bash
if(a=2):
    printf("9");
```
- Option 2
```bash
if(a==2):
    printf("9");
```
- Option 3
```bash
if(a==2) {
    printf("9");
}
```
- Option 4
```bash
if(a=2) {
    printf("9");
}
```
- Option 1
- Option 2
- Option 3
- Option 4


### Question 52

**What will be printed by the given code ? [See Answer](#answer52)**
```bash
#include <stdio.h>

int main() {
    int j = 5;
    while (j > 0) {
        printf("%d ", j);
        j--;
    }
    return 0;
}
```
- 5 4 3 2 1
- 5 4 3 2 
- 5 4 3 
- 5 4 


### Question 53

**What will be printed by the given code ? [See Answer](#answer53)**
```bash
#include <stdio.h>

int main() {
    int j = 1;
    while (j <= 5) {
        printf("%d ", j);
        j++;
    }
    return 0;
}
```
- 1 2 3 4 5
- 1 2 3 4
- 1 2 3
- 1 2

### Question 54

**What will be printed by the given code ? [See Answer](#answer54)**

```bash
#include <stdio.h>

int main() {
    int k = 10;
    while (k < 5) {
        printf("%d ", k);
        k += 2;
    }
    return 0;
}
```
- 10
- 10 12
- 10 12 14
- No Output


### Question 55

**What will be the output of the given code ? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    while (1) {
        printf("Hello");
        break;
    }
    return 0;
}
```
- Hello (infinitely)
- Compilation Error
- No output
- Hello (Just Once)



### Question 56

**What will be printed by the given code ? [See Answer](#answer)**
```bash
#include <stdio.h>

int main() {
    int x = 1;
    while (x <= 10) {
        if (x % 2 == 0) {
            printf("%d ", x);
        }
        x++;
    }
    return 0;
}
```
- 1 3 5 7 9
- 2 4 6 8 10
- 1 2 3 4 5 6 7 8 9 10
- No output


### Question 57

**What will be printed by the given code ?
 [See Answer](#answer57)**
```bash
#include <stdio.h>

int main() {
    int y = 1;
    while (y >= 1 && y <= 3) {
        printf("%d ", y);
        y++;
    }
    return 0;
}
```
- 1 2 3
- 1 2 3 4 5
- No output
- 2 3 4 5


### Question 58

**What will be printed by the given code ? [See Answer](#answer58)**
```bash
#include <stdio.h>

int main() {
    int z = 1;
    while (z <= 5) {
        if (z == 3) {
            z++;
        }
        printf("%d ", z);
        z++;
    }
    return 0;
}
```
- 1 2 3
- 1 2 3 4 5
- 1 2 4 5
- Compilation Error


### Question 59

**Write a C program that calculates and prints the sum of all even numbers from 1 to a given positive integer n. Use a while loop to iterate through the numbers. [See Answer](#answer59)**

### Question 60

**Write a C program that takes an integer as input and prints its reverse. Use a while loop for the reversal process. [See Answer](#answer60)** <br>Ex- 1234 output = 4321


### Question 61

**Given a positive integer <br>
N<br>
N, find sum of its digits. [See Answer](#answer)** <br>Ex-1234 output = 10


### Question 10

** [See Answer](#answer)**

-
-
-
-

### Question 10

** [See Answer](#answer)**

-
-
-
-

### Question 10

** [See Answer](#answer)**

-
-
-
-


### Question 10

** [See Answer](#answer)**

-
-
-
-


### Question 10

** [See Answer](#answer)**

-
-
-
-

### Question 10

** [See Answer](#answer)**

-
-
-
-

### Answer1:

**Correct Answer**: `printf()`;

```bash
Explanation:
printf() is a function in the C programming language that is used to print formatted text to the standard output.
```

### Answer2:

**Correct Answer**: `2`;

```bash
Explanation:
In the code, 5 / 2 performs integer division.
Integer division in C truncates any fractional part and returns only the integer portion of the result.
So, 5 / 2 equals 2, and that's what gets printed by printf().
```

### Answer3:

**Correct Answer**: `Hello, world!`;

```bash
Explanation:
The two printf statements will print consecutively.

In the code snippet, printf("Hello, "); prints "Hello, " to the console.
Then, printf("world!"); prints "world!" to the console.

Since there is no newline character ('\n') at the end of either printf() statement, the output will appear on the same line.
```

### Answer4:

**Correct Answer**: `printf("%d", 9*12);`;

```bash
Explanation:
9 * 12 = 108

The correct output function in C is printf()
```

### Answer5:

**Correct Answer**: `printf("%d", 9-3);`;

```bash
Explanation:
The expression 9-3 is directly used as an argument to the %d format specifier within the printf statement.
```

### Answer6:

**Correct Answer**: `5 Undefined Value`;

```bash
Explanation:
The second printf() statement in the code snippet printf("%d", 10/2.00 + 1); invokes undefined behavior because it attempts to use %d format specifier to print a floating-point value. This is because the expression 10/2.00 + 1 results in a floating-point value (6.00), but %d expects an integer argument.

Therefore, the behavior of this statement is not guaranteed and may produce different outputs on different compilers or even different runs on the same compiler. It might print garbage values.

```

### Answer7:

**Correct Answer**: `printf("%c", '9');`;

```bash
Explanation:
The %c format specifier is used in the printf statement to print as a character.

```

### Answer8:

**Correct Answer**: `1`;

```bash
Explanation:
The modulus operator '%' gives the remainder of the division, so 10 % 3 equals 1.

```

### Answer9:

**Correct Answer**: <pre>Hello
And Welcome John</pre>

```bash
Explanation:
The printf function is used to print the string "Hello\nAnd Welcome John".
\n is the escape sequence for a newline character, so "Hello" and "And Welcome John" will be printed on separate lines.
```

### Answer10:

**Correct Answer**: `B`;

```bash
Explanation:
When we print the character represented by ch + 1, it will print 'B', because the next character to 'A' is 'B'
```

### Answer11:

**Correct Answer**: `Undefined`;

```bash
Explanation:
The format specifier %f is used to print floating-point numbers. However, in this code, we're trying to print an integer value 10 using %f. This can lead to undefined behavior because the printf function expects a floating-point number when we use %f, but we're providing an integer.
```

### Answer12:

```bash

int main() {
	// your code goes here
	printf("%d",(4+8));

}

Output --> 12
```

### Answer13:

```bash
int main() {
	// your code goes here
	printf("$");

}

Output --> $
```

### Answer14:

**Correct Answer**: `Hello World!`;

```bash
Explanation:
Each printf statement prints its content sequentially, so "Hello " and "World!" will be printed together.
```

### Answer15:

**Correct Answer**: `printf("Hello\nWorld!");`;

```bash
Explanation:
The \n escape sequence is used to print on a new line.
```

### Answer16:

**Correct Answer**: `1 + 2 = 3`;

```bash
Explanation:
The expression 1 + 2 is evaluated and printed using the %d format specifier and the remaining string in the prefix is printed as it is

```

### Answer17:

**Correct Answer**: `Prints on and multiple lines`;

```bash
Explanation:
Here the %s format specifier takes the string for printing in order of their presence in the printf statement
```

### Answer18:

**Correct Answer**: `ProgrammingLanguage`;

```bash
Explanation:
The two strings will be printed as separate statements with no space in between them

```

### Answer19:

**Correct Answer**: <pre>1
2
3 </pre>

```bash
Explanation:
This uses the \n escape sequence to print each number on a new line.
```

### Answer20:

**Correct Answer**: `This is a backslash: \`;

```bash
Explanation:
Explanation:
The double backslash \\ is used to print a single backslash.
```

### Answer21:

**Correct Answer**: <pre>Hello, how are you?
I'm fine.</pre>;

```bash
Explanation:
The first printf() statement prints "Hello, " to the console.

The second printf() statement prints "how are you?" to the console followed by a newline character (\n), which moves the cursor to the beginning of the next line.

The third printf() statement prints "I'm fine." to the console, which starts on the same line where "how are you?" ends due to the presence of the newline character in the previous printf() statement.
```

### Answer22:

```bash
#include <stdio.h>

int main() {
	// your code goes here
	printf("The result of 5 + 3 is:\n%d",5+3);

}

```

### Answer23:

```bash
#include <stdio.h>

int main() {
    int i,j,n=4;
   for (i = 1; i <= n; i++) {
        // Print spaces
        for (j = 1; j <= n - i; j++) {
            printf(" ");
        }
        // Print asterisks
        for (j = 1; j <= (2 * i - 1); j++) {
            printf("*");
        }
        // Move to the next line
        printf("\n");
    }

}

```

### Answer24:

**Correct Answer**: <pre>In the
middle of difficulty
lies opportunity</pre>;

```bash
Explanation:
When this printf statement is executed, it prints the string literal to the standard output. Because of the newline characters (\n), it will produce the following output:


In the
middle of difficulty
lies opportunity

```

### Answer25:

**Correct Answer**: <pre>1
1 2
1 2 3
1 2 3 4</pre>;

```bash
Explanation:
The output of the code would be:

1
1 2
1 2 3
1 2 3 4


Explanation:
- The `printf` function is used to print formatted output to the standard output.
- Each line in the `printf` statement contains numbers separated by spaces.
- `\n` is used to print a newline character, which moves the cursor to the next line after printing.
- So, each `printf` statement prints a separate line of numbers according to the pattern specified.

```

### Answer26:

**Correct Answer**:

<pre>  
              *
            * * 
          * * * 
        * * * * 
      * * * * *
  </pre>

```bash
Explanation:
The output of the code would be:

        *
      **
    ***
  ****
*****


Explanation:
- The `printf` function is used to print formatted output to the standard output.
- Each line in the `printf` statement contains spaces and asterisks (`*`).
- The number of spaces decreases from left to right, creating a triangular pattern, while the number of asterisks increases from left to right.
- So, each `printf` statement prints a separate line of characters according to the pattern specified.

```

### Answer27:

**Correct Answer**: `10`;

```bash
Explanation:
The code initializes an integer variable named number with the value 10 and prints the content of this variable, resulting in the output 10
```

### Answer28:

**Correct Answer**: `7.800000`;

```bash
Explanation:
The code initializes a float variable named value with the value 7.8 and prints the content of this variable, resulting in the output 7.800000
```

### Answer29:

**Correct Answer**: `A`;

```bash
Explanation:
The code declares a character variable named letter and initializes it with the character 'A', then prints the content of this variable, resulting in the output A
```

### Answer30:

**Correct Answer**: `Size of double: 8`;

```bash
Explanation:
The code prints the size of the double data type using the sizeof operator, resulting in the output Size of double: 8

```

### Answer31:

**Correct Answer**: `10 5`;

```bash
Explanation:
The code declares an integer variable named num in both the outer and inner scopes. Inside the inner scope, a new variable num with the value 10 is created and printed, resulting in the output 10 5

```

### Answer32:

**Correct Answer**: `12.200000`;

```bash
Explanation:
The code adds an integer (5) and a float (7.2), and the result is implicitly converted to a float for printing.

Hence, the output is 12.200000

```

### Answer33:

**Correct Answer**: `6`;

```bash
Explanation:
The code initializes two integer variables, x and y, with values 2 and 3 respectively. It then calculates their product (x * y = 2 * 3 = 6) and assigns the result to variable z. Finally, it prints the value of z, resulting in the output 6

```

### Answer34:

**Correct Answer**: `-126`;

```bash
Explanation:
The code initializes a character variable named character with the value 130. However, a signed char has a range from -128 to 127, so overflow occurs, and the value wraps around to -126. The output is -126

```

### Answer35:

**Correct Answer**: `string`;

```bash
Explanation:
string is not a data type in C. We create string in C using the char array instead.

```

### Answer36:

**Correct Answer**: ` 3.000000`;

```bash
Explanation:
10 / 3 evaluates to 3 (as per integer division) as both 10 and 3 are integer, then 3 gets assigned to float variable resulting in 3.000000

```

### Answer37:

```bash
#include <stdio.h>

int main() {
    int a = 5, b = 10;
    a = a+b;  
    b = a-b;  
    a = a-b; 
    printf("%d %d",a,b);
    return 0;
}

```

### Answer38:

```bash
#include <stdio.h>

int main() {
	float celsius = 20.5;

	printf("%f",((celsius * 9) /5) + 32);
	return 0;
}

```

### Answer39:

```bash
#include <stdio.h>

int main() {
    float fahrenheit = 98.3;

	printf("%f",(((fahrenheit -32) * 5)/9));
	return 0;
}

```


### Answer40:

```bash
#include <stdio.h>

int main() {
    float height = 1.82;
    float weight = 72;
    printf("%f",(weight / (height * height)));
    return 0;
}

```


### Answer41:

**Correct Answer**: <pre>5
random number</pre>

```bash
Explanation:
We are using the %d format specifier to print both an integer (x) and a float (f). However, using the %d specifier for a float type invokes undefined behavior, meaning the behavior of the code cannot be predicted reliably. 

What typically happens in such case is that the printf function interprets the binary representation of the float (f) as if it were an integer. This can result in unpredictable and incorrect output. The float value 3.4 might get interpreted as some random integer value.

```

### Answer42:

**Correct Answer**: `The code will lead to a compilation error.`;

```bash
Explanation:
The code will throw a compilation error because 'a' and 'b' are declared as char arrays, but the code is reading input as an integer.
```


### Answer43:

**Correct Answer**: `It's a pleasant day.`;

```bash
Explanation:
The correct answer is (c) It's a pleasant day. The code classifies the entered temperature into different categories based on the range.
```


### Answer44:

**Correct Answer**: `Find the largest number`;

```bash
Explanation:
The correct answer is (d) Find the largest number. The if/else construct is used to determine and print the largest of the two entered numbers in the provided code.
```


### Answer45:

**Correct Answer**: `Get ready to move. It's yellow signal`;

```bash
Explanation:
The correct answer is (b) Get ready to move. It's yellow signal. The modified code simulates a traffic light and provides instructions based on the entered signal.
```


### Answer46:

**Correct Answer**: `It's Friday!`;

```bash
Explanation:
The correct answer is (c) It's Friday!. The code  identifies and prints the day of the week based on the entered day number without using && or || concepts.
```


### Answer47:

**Correct Answer**: `Identify the age group as child, adult, or senior`;

```bash
Explanation:
The correct answer is (b) Identify the age group as child, adult, or senior. The if/else if/else construct is used to determine and print the age group based on the entered age in the provided code.
```


### Answer48:

```bash
#include <stdio.h>

int main() {
	int a,b,c;
	scanf("%d%d%d",&a,&b,&c);
	if(a > b && a> c){
	    printf("Largest: %d",a);
	}else{
	    if(b>c){
	        printf("Largest: %d",b);
	    }else{
	        printf("Largest: %d",c);
	    }
	}

}
```


### Answer49:

```bash
#include <stdio.h>

int main() {
    int a, b;

    scanf("%d %d",&a,&b);
    if((a+b)%2== 0){
        printf("YES");
    }else{
        printf("NO");
    }

    return 0;
}
```


### Answer50:

```bash
#include <stdio.h>

int main() {
    // Your code goes here
    int side1,side2,side3;
    scanf("%d %d %d",&side1,&side2,&side3);
    if((side1 == side2) && (side2 == side3) && (side1 == side3)){
        printf("Equilateral");
    }else if((side1 == side2) || (side2 == side3) || (side1 == side3)){
        printf("Isosceles");
    }else{
        printf("Scalene");
    }
    return 0;
}
```


### Answer51:

**Correct Answer**: <pre>Option 3</pre>


### Answer52:

**Correct Answer**: `5 4 3 2 1`;

```bash
Explanation:
The correct answer is (a) 5 4 3 2 1. The while loop decrements j from 5 to 1, and printf prints the current value of j in each iteration.

```


### Answer53:

**Correct Answer**: `1 2 3 4 5`;

```bash
Explanation:
The correct answer is (a) 1 2 3 4 5. The while loop increments j from 1 to 5, and printf prints the current value of j in each iteration.
```

### Answer54:

**Correct Answer**: `No output`;

```bash
Explanation:
The correct answer is (d) No output. The while loop condition is initially false, so the loop body is not executed.
```

### Answer55:

**Correct Answer**: `Hello (Just Once)`;

```bash
Explanation:
This code will output "Hello" once and then terminate. 

The while (1) loop runs indefinitely, but the break statement is encountered immediately after printing "Hello", causing the loop to exit after the first iteration. So, the output will be:

```

### Answer56:

**Correct Answer**: `2 4 6 8 10`;

```bash
Explanation:
The correct answer is (b) 2 4 6 8 10. The while loop prints even numbers between 1 and 10.
```

### Answer57:

**Correct Answer**: `1 2 3`;

```bash
Explanation:
The correct answer is (a) 1 2 3. The while loop prints numbers until y becomes 3, and then it breaks out of the loop.

```


### Answer58:

**Correct Answer**: `1 2 4 5`;

```bash
Explanation:
Output: "1 2 4 5" because the loop starts with z = 1, prints and increments z in each iteration, and z is an extra incremented when it is 3. The loop continues until z is greater than 5.

```


### Answer59:

```bash
#include <stdio.h>

int main() {
	// your code goes here
	int n,i,sum=0;
	scanf("%d",&n);
	for(i=1;i<=n;i++){
	    if(i % 2 ==0){
	        sum+= i;
	    }
	}
	printf("%d",sum);
	return 0;

}
```

### Answer60:

```bash
#include <stdio.h>

int main() {
	// your code goes here
	int n,rev=0;
	scanf("%d",&n);
	while(n>0){
	    rev =rev * 10 + n %10;
	    n/=10;
	}
	printf("%d",rev);
}
```

### Answer61:


```bash
#include <stdio.h>

int main() {
	// your code goes here
	int n,sum=0;
	scanf("%d",&n);
	while(n>0){
	    sum =sum + n %10;
	    n/=10;
	}
	printf("%d",sum);
}
```


### Answer62:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer63:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer64:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer65:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer66:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer67:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer68:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer69:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer70:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer71:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer72:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer73:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer74:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer75:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer76:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer77:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer78:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer79:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer80:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer81:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer83:

**Correct Answer**: ``;

```bash
Explanation:

```



### Answer83:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer84:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer85:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer86:

**Correct Answer**: ``;

```bash
Explanation:

```



### Answer87:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer88:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer89:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer90:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer91:

**Correct Answer**: ``;

```bash
Explanation:

```



### Answer92:

**Correct Answer**: ``;

```bash
Explanation:

```



### Answer93:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer94:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer95:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer96:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer97:

**Correct Answer**: ``;

```bash
Explanation:

```



### Answer98:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer99:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer100:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```

### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```


### Answer53:

**Correct Answer**: ``;

```bash
Explanation:

```