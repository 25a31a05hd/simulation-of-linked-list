# simulation-of-linked-list
       **ALGORITHM**  create a node
     START
       create a node
       newnode=malloc(size of node)
       read value
       newnode->data=value
       newnode->next=NULL
     STOP


       **ALGORITHM**   Insert at beginning
     START
       create newnode
       read value
       newnode->data=value
       newnode->next=head
       head=newNode
     STOP

       **ALGORITHM**   Inssert at end
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

        **ALGORITHM**  Delete from beginning
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



       
      
       
       
