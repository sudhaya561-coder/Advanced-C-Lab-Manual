## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

# Aim:
To write a C program to display stack elements using an array.
# Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
# Program:
```
#include <stdio.h>
#define MAX 100
int stack[MAX];
int top = -1;
void push(int value)
{
    if (top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top] = value;
    }
}
void pop()
{
    if (top == -1)
    {
        printf("Stack Underflow\n");
    }
    else
    {
        top--;
    }
}
void display()
{
    int i;
    if (top == -1)
    {
        printf("Stack is empty\n");
    }
    else
    {
        printf("Stack elements are:\n");

        for (i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }
}
int main()
{
    int n, i, value;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("Enter element: ");
        scanf("%d", &value);
        push(value);
    }
    display();
    return 0;
}
```

# Output:
<img width="457" height="477" alt="Screenshot 2026-09-02 225047" src="https://github.com/user-attachments/assets/5711d244-a30f-4a61-9658-cd947fd74881" />




# Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
# Aim:
To create a C program to push the given element in to a stack using array.
# Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
# Program:
```
#include <stdio.h>
#define MAX 100
float stack[MAX];
int top = -1;
void push(float value)
{
    if (top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top] = value;
        printf("%.2f pushed into stack\n", value);
    }
}
int main()
{
    int n, i;
    float value;
    printf("Enter number of elements to push: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("Enter element: ");
        scanf("%f", &value);
        push(value);
    }
    return 0;
}
```

# Output:
<img width="531" height="426" alt="Screenshot 2026-09-02 225412" src="https://github.com/user-attachments/assets/a0a4a7e5-a252-41e6-a3f4-84a91c2b3eba" />





# Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
# Aim:
To write a C program to display queue elements using array

# Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
# Program:
```
#include <stdio.h>
int queue[100], front = 0, rear = -1;
void display()
{
    int i;
    for (i = front; i <= rear; i++)
        printf("%d ", queue[i]);
}
int main()
{
    int n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        scanf("%d", &queue[++rear]);
    }
    printf("Queue elements are: ");
    display();
    return 0;
}
```
# Output:

<img width="543" height="338" alt="Screenshot 2026-09-02 225722" src="https://github.com/user-attachments/assets/c4cdebd9-047e-40e2-8d29-cf56effbb131" />



# Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
# Aim:
To write a C program to insert elements in queue using array.

# Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

# Program:
```
#include <stdio.h>
int queue[100];
int front = 0, rear = -1;
void enqueue(int x)
{
    rear++;
    queue[rear] = x;
}
int main()
{
    int n, i, x;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for(i = 0; i < n; i++)
    {
        printf("Enter element: ");
        scanf("%d", &x);
        enqueue(x);
    }
    printf("Queue elements are: ");
    for(i = front; i <= rear; i++)
        printf("%d ", queue[i]);
    return 0;
}
```
# Output:

<img width="437" height="260" alt="Screenshot 2026-09-02 230003" src="https://github.com/user-attachments/assets/81d60c04-6482-4774-a041-cd3fe33a7fb9" />


# Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



# Aim:

To create a function in C that deletes an element from a queue implemented using an array.

# Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



# Program:

```
#include <stdio.h>
int queue[100];
int front = 0, rear = 2;
void delete()
{
    if (front > rear)
        printf("Queue is empty");
    else
    {
        printf("Deleted element: %d", queue[front]);
        front++;
    }
}
int main()
{
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;
    delete();
    return 0;
}
```

# Output:

<img width="440" height="192" alt="Screenshot 2026-09-02 230340" src="https://github.com/user-attachments/assets/9db8e731-1375-4da0-b6a8-8322789c46e9" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
