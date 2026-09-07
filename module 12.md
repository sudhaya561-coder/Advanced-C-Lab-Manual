## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
# Aim:
To write a C program to display stack elements using linked list.

# Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
# Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
int main()
{
    struct Node *top = NULL, *newNode, *temp;
    int n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for(i = 0; i < n; i++)
    {
        newNode = (struct Node*)malloc(sizeof(struct Node));
        printf("Enter element: ");
        scanf("%d", &newNode->data);
        newNode->next = top;
        top = newNode;
    }
    printf("Stack elements are:\n");
    temp = top;
    while(temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }
    return 0;
}
```

# Output:


<img width="482" height="367" alt="Screenshot 2026-09-02 233835" src="https://github.com/user-attachments/assets/a25a1a48-0cfa-4053-9b0f-e345b0fe5967" />



# Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
# Aim:
To write a C program to pop an element from the given stack using liked list.

# Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
# Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

int main()
{
    struct Node *top = NULL, *newNode, *temp;
    int n, i;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    // Push elements into stack
    for(i = 0; i < n; i++)
    {
        newNode = (struct Node*)malloc(sizeof(struct Node));

        printf("Enter element: ");
        scanf("%d", &newNode->data);

        newNode->next = top;
        top = newNode;
    }

    // Pop element
    if(top == NULL)
    {
        printf("Stack is empty");
    }
    else
    {
        temp = top;
        printf("Popped element = %d\n", top->data);
        top = top->next;
        free(temp);
    }

    // Display remaining stack
    printf("Stack after POP:\n");

    temp = top;

    while(temp != NULL)
    {
        printf("%d\n", temp->data);
        temp = temp->next;
    }

    return 0;
}
```

# Output:


<img width="425" height="378" alt="Screenshot 2026-09-02 234016" src="https://github.com/user-attachments/assets/3c571377-de6c-4d29-bd5e-accefc75af00" />




# Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
# Aim:
To write a C program to display queue elements using linked list.
# Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
# Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
int main()
{
    struct Node *front = NULL, *rear = NULL;
    struct Node *newNode, *temp;
    int n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    // Insert elements into queue
    for(i = 0; i < n; i++)
    {
        newNode = (struct Node*)malloc(sizeof(struct Node));
        printf("Enter element: ");
        scanf("%d", &newNode->data);
        newNode->next = NULL;
        if(front == NULL)
        {
            front = rear = newNode;
        }
        else
        {
            rear->next = newNode;
            rear = newNode;
        }
    }

    // Display queue
    printf("Queue elements are:\n");
    temp = front;
    while(temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    return 0;
}
```

# Output:


<img width="452" height="321" alt="Screenshot 2026-09-02 234209" src="https://github.com/user-attachments/assets/ba3f9228-eca6-443c-b6ae-f7db7dfeed4b" />


# Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

# Aim:
To write a C program to insert elements in queue using linked list

# Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
# Program:
```
#include <stdio.h>
#include <stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
int main()
{
    struct Node *front = NULL, *rear = NULL;
    struct Node *newNode;
    int n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for(i = 0; i < n; i++)
    {
        newNode = (struct Node*)malloc(sizeof(struct Node));
        printf("Enter element: ");
        scanf("%d", &newNode->data);
        newNode->next = NULL;
        if(front == NULL)
        {
            front = rear = newNode;
        }
        else
        {
            rear->next = newNode;
            rear = newNode;
        }
    }
    printf("Queue elements are:\n");
    newNode = front;
    while(newNode != NULL)
    {
        printf("%d ", newNode->data);
        newNode = newNode->next;
    }
    return 0;
}
```

# Output:


<img width="430" height="323" alt="Screenshot 2026-09-02 234356" src="https://github.com/user-attachments/assets/38e5e12e-f402-4ff9-b5d3-9acd3b826677" />


# Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


# Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

# Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

# Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
int peek(struct Node *front)
{
    if (front == NULL)
    {
        printf("Queue is empty");
        return -1;
    }
    return front->data;
}
int main()
{
    struct Node *front;
    front = malloc(sizeof(struct Node));
    front->data = 10;
    front->next = NULL;
    printf("Peek element = %d", peek(front));
    return 0;
}
```

# Output:

<img width="405" height="192" alt="Screenshot 2026-09-02 234620" src="https://github.com/user-attachments/assets/12946340-4f67-4244-bfe1-e6b21bb3e4dc" />




# Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


