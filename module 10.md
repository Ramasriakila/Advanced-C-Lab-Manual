EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char data)
{
    struct Node* temp;
    temp = head;
    char item = data;
    int i = 1;
    if(temp == NULL)
    {
        printf("No elements\n");
    }
    else
    {
        while (temp != NULL) 
        {
            if (temp->data == item) 
            {
                printf("item %c found at location %d\n", item, i);
                return;
            }
            temp = temp->next;
            i++;    
        }
        printf("Item not found\n");
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/f18ee647-dfb5-4fcc-8df4-2d43b039cd14)

Result:
Thus, the program to search a given element in the given linked list is verified successfully.

EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```
struct Node{
    int data; 
    struct Node *next;
}*head;


void insert(int data)
{
    struct Node *temp, *n;
    n = (struct Node*)malloc(sizeof(struct Node));
    if(head == NULL)
    {
        head = n;
        head->data = data;
    }
    else
    {
        n->data = data;
        n->next = NULL;
        temp = head;
        while(temp->next != NULL)
            temp = temp->next;
        temp->next = n;
    }
    
}
```
Output:
![image](https://github.com/user-attachments/assets/2b202fda-33ae-4620-86e9-a094d6ca597b)

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void display()
{
    struct Node *temp;
    temp = head;
    while(temp != NULL)
    {
        printf("%d ",temp->data);
        temp = temp->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/a87f9c4a-9dd4-45ba-9065-52b4633179d0)


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *n, *temp;
    n = (struct Node*)malloc(sizeof(struct Node));
    n->data = data;
    n->next = NULL;
    n->prev = NULL:
    if(head == NULL)
    {
        head = n;
        head->data = data;
    }
    else
    {
        temp = head;
        while(temp->next != NULL)
        {
            temp = temp->next;
        }
        temp->next = n;
        n->prev = temp;
    }
}

```
Output:

![image](https://github.com/user-attachments/assets/a838706c-637b-4af0-9341-34a62cf79982)



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.


EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
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


Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void delete()
{
    struct Node *temp;
    temp = head;
    if(head == NULL)
    {
        printf("UNDERFLOW\n");
    }
    else if(head->next == NULL)
    {
        head = NULL;
        free(head);
        printf("node deleted\n");
    }
    else
    {
        temp = head;
        head = head->next;
        free(temp);
        printf("node deleted\n");
    }
}
```
Output:


![image](https://github.com/user-attachments/assets/e63bb099-c190-4b76-86ad-a8f5992505dc)




Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





