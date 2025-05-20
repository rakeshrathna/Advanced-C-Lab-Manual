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
    char item=data;
    int i=0,f=0;
    struct Node*temp;
    temp=head;
    if(temp==NULL){
        printf("Item not found");
    }
    else{
        while(temp!=NULL){
            if(temp->data==item){
                printf("item %c found at location %d",item,i+1);
              
              f=1;
            }
            i++;
            temp=temp->next;      
        }        
    }
    if(f==0)
    {
                printf("Item not found");
    }
}
```

Output:

![444787886-267cf469-ff07-4bb9-801c-40f79c478758](https://github.com/user-attachments/assets/45995b33-0960-484d-85f8-4a29af7ecee5)



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
    char data; 
    struct Node *next;
}*head;

void insert(char data)
{
    struct Node *newnode,*temp;
    newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    if(head==NULL){
        head=newnode;
    }
    else{
        temp=head;
        while(temp->next!=NULL){
            temp=temp->next;
        }
        temp->next=newnode;
    }
    
}
```
Output:

![444787913-0819b0f4-6fc1-4e32-be3e-e95c05baf662](https://github.com/user-attachments/assets/337ee106-2313-4cca-a6f5-a22ef9058498)

 
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
    struct Node*temp;
    temp=head;
    while(temp!=NULL){
        printf("%d\n",temp->data);
        temp=temp->next;
    }        
}
```

Output:

![444787988-049c4a5d-f339-4456-9744-002ee73c64a3](https://github.com/user-attachments/assets/acd5b86f-c80b-4b4c-b2a9-6815a0bff6a9)


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
    float data;
    struct Node *prev;
    struct Node *next;
}*head;

void insert(float data)
{
    struct Node *temp,*newnode;
    newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    newnode->prev=NULL;
    if(head==NULL){
        head=newnode;
    }
    else{
        temp=head;
        while(temp->next!=NULL){
            temp=temp->next;
        }
        temp->next=newnode;
        newnode->prev=temp;
    }        
}
```

Output:

![444788034-f3c560e6-4042-4f15-b1d2-b4bb4641f009](https://github.com/user-attachments/assets/696529a7-0200-455b-ace5-7ee1704dfbfc)


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
    int data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node *ptr;
    if(head == NULL)
    {
        printf("List is empty\n");
    }
    else
    {
        ptr = head;
        head = ptr->next;
        free(ptr);
        printf("Node deleted from the begining ...\n");
    }
}
```

Output:


![444788082-02728230-c669-4659-acb6-7e684a87ee2c](https://github.com/user-attachments/assets/1c8ee055-a84a-4774-9b90-36b72dca564c)





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





