## EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

## Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

## Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
## Program:
```
#include <stdio.h>
struct eligible
{
    int age;
    char n[50];
};
int main()
{
    struct eligible e;
    scanf("%d", &e.age);
    scanf("%s", e.n);
    if (e.age <= 6)
        printf("Vaccine Eligibility: No");
    else
        printf("Vaccine Eligibility: Yes");
    printf("\n%d", e.age);
    printf("\n%s", e.n);
    return 0;
}
```

## Output:
<img width="398" height="246" alt="Screenshot 2026-07-31 114944" src="https://github.com/user-attachments/assets/31fc6231-c442-48a7-a21a-3bd68304b9f2" />




## Result:
Thus, the program is verified successfully. 



## EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION

## Aim:
To write a C program for passing structure as function and returning a structure from a function

# Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
# Program:
```
#include <stdio.h>

struct numbers
{
    int a;
    int b;
};
int add(struct numbers n)
{
    return n.a + n.b;
}
int main()
{
    struct numbers n;
    printf("value of a: ");
    scanf("%d", &n.a);
    printf("value of b: ");
    scanf("%d", &n.b);
    printf("Sum = %d", add(n));
    return 0;
}
```




# Output:

<img width="1377" height="601" alt="Screenshot 2026-07-28 115253" src="https://github.com/user-attachments/assets/1a219a2c-37c9-46ff-aaba-b318072b0bc7" />





# Result:
Thus, the program is verified successfully


 
## EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

# Aim:
To write a C program to read a file name from user

# Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
# Program:

<img width="617" height="541" alt="Screenshot 2026-09-02 185837" src="https://github.com/user-attachments/assets/0ef616d5-ec95-4f53-9297-5d25288d870f" />



# Output:


<img width="548" height="272" alt="Screenshot 2026-09-02 185847" src="https://github.com/user-attachments/assets/68c6425f-21d3-4990-b6fd-02c0a56c9571" />




# Result:
Thus, the program is verified successfully
 


## EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE

# Aim:
To write a C program to read, a file and insert text in that file
# Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
# Program:

<img width="678" height="606" alt="Screenshot 2026-09-02 221613" src="https://github.com/user-attachments/assets/496f2def-f278-4fb2-b149-93a89f81d841" />



# Output:

<img width="522" height="83" alt="Screenshot 2026-09-02 221624" src="https://github.com/user-attachments/assets/504744c3-12a1-4c6d-9d68-76b398a5be92" />




# Result:
Thus, the program is verified successfully



## Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

# Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

# Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

# Program:

<img width="718" height="695" alt="Screenshot 2026-09-02 221903" src="https://github.com/user-attachments/assets/02afa9bf-255e-4179-97d3-6d1d503389db" />



# Output:

<img width="455" height="451" alt="Screenshot 2026-09-02 221909" src="https://github.com/user-attachments/assets/547cc523-3819-40e8-be70-8b4334587ebe" />




Result:
Thus, the program is verified successfully
