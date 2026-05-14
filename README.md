# simulation-of-linked-list
       **ALGORITHM**  CREATE A NODE
     START
       create a node
       newnode=malloc(size of node)
       read value
       newnode->data=value
       newnode->next=NULL
     STOP


       **ALGORITHM**  INSERT AT BEGINNING
     START
       create newnode
       read value
       newnode->data=value
       newnode->next=head
       head=newNode
     STOP

       **ALGORITHM**  INSERT AT END
     START
       create a newnode
       read value
       newnode->data=value
       newnode->next=NULL
       IF head==NULL
        head=newnode
        ELSE
        tewmp=head
        WHILE temp->next!=NULL
        temp=temp->next
        END WHILE
        temp->next=newnode
        END IF
       STOP

        **ALGORITHM**  DELETE FROM BEGINNING
       START
        IF head==NULL
        PRINT "list is empty"
        ELSE
        temp=head
        head=head->next
        FREE temp
        END IF
       STOP 

        **ALGORITHM**  DISPLAY LINKED LIST
      START
        temp=head
        IF temp==NULL
        PRINT "list is empty"
        ELSE
        WHILE temp!=NULL
        PRINT temp->data
        temp=temp->next
        END WHILE
        END IF
      STOP

      **ALGORITHM**  SEARCH ELEMENT
    START
     temp=head
     read key
     WHILE temp!=NULL
     IF temp->data==key
     PRINT "element found"
     EXIT
     END IF
     temp=temp->next
     END WHILE
     PRINT "element not found"
    STOP

 FLOWCHART
 <img width="1024" height="1536" alt="Image" src="https://github.com/user-attachments/assets/527b9a6e-fc1c-4b7b-85fa-09ca3e5df343" />

 METHODOLOGY
 A methodology for simulation of a linked list explains how linked lists are represented and operated in a simulated environment, usually using arrays and indices instead of dynamic memory pointers. This approach is commonly used in data structures labs, embedded systems, and educational simulations.

Methodology for Simulation of Linked List
1. Introduction

A linked list is a dynamic data structure where each node contains:

Data
Link (pointer/index) to the next node

In simulation, actual memory pointers are replaced by array indices.

2. Structure of Simulated Linked List

Two arrays are generally used:

Array	Purpose
INFO[]	Stores data values
LINK[]	Stores index of next node

Additional variables:

START → index of first node
AVAIL → beginning of free node list
3. Node Representation

A node consists of:

INFO	LINK
Data	Address/Index of next node

Example:

Index	INFO	LINK
1	10	4
4	20	7
7	30	-1

START = 1

This represents:

10 → 20 → 30 → NULL
4. Initialization Methodology

Initially:

All nodes are free
Free nodes are connected together through LINK[]

Example:

Index	LINK
1	2
2	3
3	4
4	-1

AVAIL = 1

5. Operations in Simulated Linked List
A. Insertion
Steps
Take first free node from AVAIL
Store data in INFO
Adjust links
Update START
Algorithm
1. NEW = AVAIL
2. AVAIL = LINK[AVAIL]
3. INFO[NEW] = ITEM
4. LINK[NEW] = START
5. START = NEW
B. Deletion
Steps
Locate node
Adjust previous node link
Return deleted node to AVAIL list
Algorithm
1. TEMP = START
2. START = LINK[START]
3. LINK[TEMP] = AVAIL
4. AVAIL = TEMP
C. Traversal
Steps
Start from START
Visit each node
Move using LINK
Algorithm
PTR = START
WHILE PTR ≠ -1
    PRINT INFO[PTR]
    PTR = LINK[PTR]
END WHILE
6. Advantages of Simulation
No need for actual pointers
Easier to understand
Useful in languages without pointer support
Good for teaching and debugging
7. Disadvantages
Fixed size arrays
Memory wastage possible
Slower than real linked lists
Limited dynamic allocation
8. Applications
Educational demonstrations
Memory management simulation
Static memory environments
Compiler and operating system concepts
9. Conclusion

Simulation of linked lists uses arrays and indices to imitate dynamic memory allocation. The methodology involves maintaining data and link arrays along with free-space management through the AVAIL list. It is widely used for understanding linked list operations such as insertion, deletion, and traversal without using actual pointers.
