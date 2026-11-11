#include<stdio.h>
#include<string.h>
#include<stdlib.h>
#include<unistd.h>
typedef struct student
{
    int rollno;
    char name[50];
    float marks;
    struct student *next;
}SLL;

void addtherecord(SLL **);
void deletetherecord(SLL **);
void showthelist(SLL *);
void modifytherecord(SLL *);
void savetherecord(SLL *);
void exittherecord(SLL **);
void sortthelist(SLL *);
void deleteAll(SLL **);
void reversetherecord(SLL *);


int main()
{
    SLL *headptr=0;
    int op,c;
    while(1)
        {
            printf("\033[34m *-*-*-*- STUDENT RECORD MENU *-*-*-*-*\n");
            printf("1.ADD NEW RECORD\n2.DELETE A RECORD\n3.SHOW THE LIST\n4.MODIFY A RECORD\n5.SAVE RECORD \n6.EXIT\n7.SORT THE LIST\n8.DELETE ALL THE RECORDS\n9.REVERSE THE LIST\n \033[0m" );
            printf("\033[33mEnter your Choice:\n \033[0m");
            scanf("%d",&op);
    switch(op)
        {
            case 1:addtherecord(&headptr);
                    break;
            case 2:deletetherecord(&headptr);
                    break;
            case 3:showthelist(headptr);
                    break;
            case 4:modifytherecord(headptr);
                    break;
            case 5:savetherecord(headptr);
                    break;
            case 6:exittherecord(&headptr);
                    break;
            case 7:sortthelist(headptr);
                    break;
           case 8:deleteAll(&headptr);
                    break;
            case 9:reversetherecord(headptr);
                    break;
            
        }
    }
}

    void addtherecord(SLL **ptr)
{
    SLL *new;
    new=malloc(sizeof(SLL));
    printf("Enter the Roll No,Name and Marks:\n");
    scanf("%d %s %f",&new->rollno,new->name,&new->marks);
    new->next=0;
    if(*ptr==0)
     *ptr=new;
    else
    {
        SLL *last=*ptr;
        while(last->next)
        last=last->next;
        
        last->next=new;
    }
}

   void showthelist(SLL *ptr)
{
    if(ptr==0)
    {
        printf("No records Found");
        return;
    }
    while(ptr)
    {
        printf("%d %s %f\n",ptr->rollno,ptr->name,ptr->marks);
        ptr=ptr->next;
    }
}

void modifytherecord(SLL *ptr)
{
    if(ptr==0)
    {
        printf("No record Found\n");
        return;
    }

    int num;
    printf("Enter Roll No to modify:\n");
    scanf("%d",&num);

    while(ptr)
    {
        if(num==ptr->rollno)
        {
            printf("Enter new Name:\n");
            scanf("%s",ptr->name);

            printf("Record modification Completed \n");
            return;
        }

        ptr=ptr->next;
    }

    printf("Roll  No not found\n");
}

  void deletetherecord(SLL **ptr)
{
    if(*ptr==0)
    {
        printf("no records found\n");
        return;
    }
    int num;
    printf("Enter Roll No to delete:\n");
    scanf("%d",&num);
    SLL *del=*ptr,*prev;
    while(del)
        {
            if(num==del->rollno)
            {
                if(*ptr==del)
                    *ptr=del->next;
                else
                    prev->next=del->next;
                free(del);
                return;
            }
            prev=del;
            del=del->next;
        }
    printf("Roll no not found\n");
}

void savetherecord(SLL *ptr)
{
    if(ptr==0)
    {
        printf("No record found\n");
        return;
    }
    FILE *fp=fopen("std.txt","w");
    while(ptr)
        {
            fprintf(fp,"%d %s %f\n",ptr->rollno,ptr->name,ptr->marks);
            ptr=ptr->next;
        }
    printf("Data saved in file\n");
    fclose(fp);
}

void exittherecord(SLL **ptr)
{
    SLL *temp;
    while(*ptr)
        {
            temp=*ptr;
            *ptr=(*ptr)->next;
            free(temp);
        }
    printf(" Exit Successful");
    exit(0);
}

void sortthelist(SLL *ptr)
{
    int countnode(SLL *ptr)
{
    int c=0;
    while(ptr)
    {
        c++;
        ptr=ptr->next;
    }
    return c;
}
    if(ptr==0)
    {
        printf("No records Found\n");
        return;
    }
    SLL *p1=ptr, *p2,t;
    int i,j,c=countnode(ptr);
    for(i=0;i<c-1;i++)
    {
        p2=p1->next;
        for(j=0;j<c-1-i;j++)
        {
            if(strcmp(p1->name,p2->name)>0)
            {
                t.rollno=p1->rollno;
                strcpy(t.name,p1->name);
                t.marks=p1->marks;
                
                p1->rollno=t.rollno;
                strcpy(p1->name,p2->name);
                p1->marks=p2->marks;
                
                p2->rollno=t.rollno;
                strcpy(p2->name,t.name);
                p2->marks=t.marks;
            }
            p2=p2->next;
        }
        p1=p1->next;
    }
}

void deleteAll(SLL **ptr)
{
    if(*ptr==0)
    {
        printf("No Records Found");
        return;
    }
    SLL *del=*ptr;
    int c=1;
    while(del)
    {
        *ptr=del->next;
        printf("Node position:%d has been deleted\n",c++);
        sleep(1);
        free(del);
        del=*ptr;
    }
    printf("All Records deleted\n");
}

void reversetherecord(SLL *ptr)
{
    int countnode(SLL *ptr)
{
    int c=0;
    while(ptr)
    {
        c++;
        ptr=ptr->next;
    }
    return c;
}
    if(ptr==0)
    {
        printf("No Records found");
    }
    SLL *t;
    int i,j,c=countnode(ptr);
    for(i=0;i<c;i++)
    {
        t=ptr;
        for(j=0;j<c-1-i;j++)
         t=t->next;
         printf("%d %s %f\n",t->rollno,t->name,t->marks);
    }
}
