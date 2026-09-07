# Aim:
To write a C program to search a given element in the given linked list.

# Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
# Program:

```
#include <stdio.h>
#include <stdlib.h>
struct node
{
    int data;
    struct node *next;
};
void search(struct node *head, int key)
{
    int pos = 1;
    while (head != NULL)
    {
        if (head->data == key)
        {
            printf("Element found at position %d", pos);
            return;
        }
        head = head->next;
        pos++;
    }
    printf("Element not found");
}
int main()
{
    struct node *head, *second, *third;
    int key;
    head = malloc(sizeof(struct node));
    second = malloc(sizeof(struct node));
    third = malloc(sizeof(struct node));
    head->data = 10;
    head->next = second;
    second->data = 20;
    second->next = third;
    third->data = 30;
    third->next = NULL;
    printf("Enter element to search: ");
    scanf("%d", &key);
    search(head, key);
    return 0;
}
```

# Output:
<img width="402" height="222" alt="Screenshot 2026-09-02 230835" src="https://github.com/user-attachments/assets/30fbcdd4-b17b-4bfc-bc0d-449a404ab46c" />





# Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
# Aim:
To write a C program to insert a node in a linked list.
# Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
# Program:

```

#include <stdio.h>
#include <stdlib.h>
struct node
{
    char data;
    struct node *next;
};
void insert(struct node **head, char value)
{
    struct node *newnode, *temp;
    newnode = malloc(sizeof(struct node));
    newnode->data = value;
    newnode->next = NULL;
    if (*head == NULL)
    {
        *head = newnode;
    }
    else
    {
        temp = *head;
        while (temp->next != NULL)
            temp = temp->next;

        temp->next = newnode;
    }
}
int main()
{
    struct node *head = NULL;
    insert(&head, 'A');
    insert(&head, 'B');
    insert(&head, 'C');
    printf("Linked List: ");
    while (head != NULL)
    {
        printf("%c ", head->data);
        head = head->next;
    }
    return 0;
}
```

# Output:


<img width="440" height="202" alt="Screenshot 2026-09-02 231353" src="https://github.com/user-attachments/assets/5011479c-6de1-4b39-9c56-024cc50c33da" />


 
# Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
# Aim:
To write a C program to traverse a doubly linked list.

# Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
# Program:

```
#include <stdio.h>
#include <stdlib.h>
struct node
{
    int data;
    struct node *prev;
    struct node *next;
};
int main()
{
    struct node *head, *second, *third, *temp;
    head = malloc(sizeof(struct node));
    second = malloc(sizeof(struct node));
    third = malloc(sizeof(struct node));
    head->data = 10;
    head->prev = NULL;
    head->next = second;
    second->data = 20;
    second->prev = head;
    second->next = third;
    third->data = 30;
    third->prev = second;
    third->next = NULL;
    temp = head;
    printf("Doubly Linked List: ");
    while (temp != NULL)
    {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    return 0;
}
```

# Output:


<img width="438" height="202" alt="Screenshot 2026-09-02 231540" src="https://github.com/user-attachments/assets/e6963726-cc4a-42fd-b6bb-933488197221" />



# Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
# Aim:
To write a C program to insert an element in doubly linked list

# Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
# Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *prev;
    struct Node *next;
};
int main() {
    struct Node *head = NULL, *newNode, *temp;
    int n, i;
    printf("Enter number of nodes: ");
    scanf("%d", &n);
    for(i = 0; i < n; i++) {
        newNode = (struct Node*)malloc(sizeof(struct Node));
        printf("Enter data: ");
        scanf("%d", &newNode->data);
        newNode->prev = NULL;
        newNode->next = NULL;

        if(head == NULL) {
            head = newNode;
        }
        else {
            temp = head;

            while(temp->next != NULL)
                temp = temp->next;

            temp->next = newNode;
            newNode->prev = temp;
        }
    }

    // Insert a new element at the end
    newNode = (struct Node*)malloc(sizeof(struct Node));

    printf("Enter element to insert: ");
    scanf("%d", &newNode->data);

    newNode->next = NULL;

    temp = head;

    while(temp->next != NULL)
        temp = temp->next;

    temp->next = newNode;
    newNode->prev = temp;

    // Display the list
    printf("\nDoubly Linked List: ");

    temp = head;

    while(temp != NULL) {
        printf("%d <-> ", temp->data);
        temp = temp->next;
    }

    printf("NULL\n");

    return 0;
}
```

# Output:


<img width="612" height="338" alt="Screenshot 2026-09-02 231711" src="https://github.com/user-attachments/assets/d8f72a5e-03b9-4345-82dd-8052264be86e" />



# Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




# Aim:
To write a C function that deletes a given element from a linked list.

# Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


# Program:

```
#include <stdio.h>
#include <stdlib.h>
struct Node
{
    int data;
    struct Node *next;
};
struct Node* deleteElement(struct Node *head, int key)
{
    struct Node *temp = head;
    struct Node *prev = NULL;
    if (head == NULL)
    {
        printf("List is empty\n");
        return head;
    }
    if (temp->data == key)
    {
        head = temp->next;
        free(temp);
        return head;
    }
    while (temp != NULL && temp->data != key)
    {
        prev = temp;
        temp = temp->next;
    }
    if (temp == NULL)
    {
        printf("Element not found\n");
        return head;
    }
    prev->next = temp->next;
    free(temp);
    return head;
}
int main()
{
    struct Node *head, *second, *third;
    int key;
    head = malloc(sizeof(struct Node));
    second = malloc(sizeof(struct Node));
    third = malloc(sizeof(struct Node));
    head->data = 10;
    head->next = second;
    second->data = 20;
    second->next = third;
    third->data = 30;
    third->next = NULL;
    printf("Enter element to delete: ");
    scanf("%d", &key);
    head = deleteElement(head, key);
    printf("Linked List: ");
    while (head != NULL)
    {
        printf("%d ", head->data);
        head = head->next;
    }
    return 0;
}
```

# Output:


<img width="417" height="217" alt="Screenshot 2026-09-02 232044" src="https://github.com/user-attachments/assets/18b49729-0325-49f2-9d07-730690a67341" />



# Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





