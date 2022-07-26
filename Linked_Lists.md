# Linked Lists

A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

### some Information abaut Linked Lists:

1.Linked List - A data structure that contains nodes that links/points to the next node in the list.
2.Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
3.Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
40Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
5.Next - Each node contains a property called Next. This property contains the reference to the next node.
Head - The Head is a reference of type Node to the first node in a linked list.
C6.urrent - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

### Traversal 

The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

When traversing through a linked list, the Current variable will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.

### Adding a Node

An example can be with adding a node to a linked list. If we want to add a node with an O(1) efficiency, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.

### how to add a node to a linked list:

1. Declare head pointer and make it as NULL.


2. Create a new node with the given data. And make the new node => next as NULL.
(Because the new node is going to be the last node.)

3. If the head node is NULL (Empty Linked List),
make the new node as the head.


4. If the head node is not null, (Linked list already has some elements),find the last node. make the last node => next as the new node.

Following are the 4 steps to add a node at the front:
Time complexity of push() is O(1) as it does a constant amount of work.

1. Declare head pointer and make it as NULL.
struct node
{
   int data;    
   struct node *next;
};

struct node *head = NULL;

2. Create a new node
void addLast(struct node **head, int val)
{
    //create a new node
    struct node *newNode = malloc(sizeof(struct node));
    newNode->data = val;
    newNode->next = NULL;
}

3. If the head node is NULL, make the new node as head

void addLast(struct node **head, int val)
{
    //create a new node
    struct node *newNode = malloc(sizeof(struct node));
    newNode->data = val;
    newNode->next     = NULL;

    

    //if head is NULL, it is an empty list
    if(*head == NULL)
    *head = newNode;   
}
4. Otherwise, find the last node and set last node => new node
The last node of a linked list has the reference pointer as NULL. i.e. node=>next = NULL.

To find the last node, we have to iterate the linked till the node=>next != NULL.

while(node->next != NULL)
{
    node = node->next;
}

### Print Out Nodes
Printing out all of the nodes in a Linked List is very similar to what we did in the Includes() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list.

Much like in Includes, we are creating a while loop to check and make sure we are not at the end of a linked list. Right before the while loop restarts, we move Current to equal the next node in the list.

Once we hit the end, we write out the null pointed to by the last node (or Head, if it’s empty).
