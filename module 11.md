## EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
# Aim:
To write a C program to create a function to find the greatest number

# Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
# Program:
```
#include <stdio.h>

int greatest(int a, int b, int c)
{
    if(a >= b && a >= c)
        return a;
    else if(b >= a && b >= c)
        return b;
    else
        return c;
}
int main()
{
    int a, b, c, result;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    result = greatest(a, b, c);
    printf("Greatest number = %d", result);
    return 0;
}
```

# Output:

<img width="401" height="227" alt="Screenshot 2026-09-02 232740" src="https://github.com/user-attachments/assets/d771b23e-74b1-4fda-acab-c907d8669ff9" />


# Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
## EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
# Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

# Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
# Program:
```
#include <stdio.h>
int main()
{
    int a, b;
    int and_result, or_result, xor_result;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    and_result = a & b;
    or_result = a | b;
    xor_result = a ^ b;
    printf("AND = %d\n", and_result);
    printf("OR = %d\n", or_result);
    printf("XOR = %d\n", xor_result);

    return 0;
}
```

# Output:

<img width="428" height="266" alt="Screenshot 2026-09-02 232900" src="https://github.com/user-attachments/assets/11e85995-df21-461c-890c-e2c76756aa33" />


# Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
## EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
# Aim:
To write a C program to write the logic for the requests

# Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
# Program:
```
#include <stdio.h>
int main()
{
    int a, b;
    int and, or, xor;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    and = a & b;
    or = a | b;
    xor = a ^ b;
    printf("AND = %d\n", and);
    printf("OR = %d\n", or);
    printf("XOR = %d\n", xor);
    return 0;
}
```

# Output:

<img width="413" height="287" alt="Screenshot 2026-09-02 233021" src="https://github.com/user-attachments/assets/5e0c7954-702b-4493-9015-4718cee70a05" />



# Result:
Thus, the program to write the logic for the requests is verified successfully.


 
## EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
# Aim:
To write a C program print the sum of the integers in the array.

# Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



# Program:
```
#include <stdio.h>
int main()
{
    int a[5], i, sum = 0;
    printf("Enter 5 integers: ");
    for(i = 0; i < 5; i++)
    {
        scanf("%d", &a[i]);
        sum = sum + a[i];
    }
    printf("Sum of integers = %d", sum);
    return 0;
}
```

# Output:

<img width="455" height="210" alt="Screenshot 2026-09-02 233153" src="https://github.com/user-attachments/assets/4652ce9c-8883-4ffe-af6d-97a97ca65b5e" />


 


# Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
## EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



# Aim:

To write a C program that counts the number of words in a given sentence.

# Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



# Program:
```
#include <stdio.h>
#include <string.h>
int main()
{
    char str[100];
    int i, words = 0;
    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);
    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] != ' ' && str[i] != '\n' &&
           (i == 0 || str[i - 1] == ' '))
        {
            words++;
        }
    }
    printf("Number of words = %d", words);
    return 0;
}
```

# Output:

<img width="432" height="236" alt="Screenshot 2026-09-02 233416" src="https://github.com/user-attachments/assets/b0139c77-21a7-48f6-bc35-e1eb173564a1" />




# Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
