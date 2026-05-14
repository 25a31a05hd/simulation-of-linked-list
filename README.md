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
    <img width="960" height="1440" alt="Image" src="https://github.com/user-attachments/assets/ab4a5e3e-1b03-42c2-9979-762d87b35557" />



       
      
       
       
