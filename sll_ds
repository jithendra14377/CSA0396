#include<stdio.h>
#include<stdlib.h>
#include<malloc.h>

struct node{
	int data;
	struct node *next;
}*head=NULL,*p,*t,*newnode;

void create(){
	int ele,i,n;
	printf("enter the no of elements:");
	scanf("%d",&n);
	for (i=1;i<=n;i++){
		printf("enter the element");
		scanf("%d",&ele);
		newnode=(struct node*)malloc(sizeof(struct node));
		newnode->data=ele;
		newnode->next=NULL;
		if(head==NULL)
		{
			head=newnode;
			p=newnode;
		}
		else
		{
			for(p=head;p->next!=NULL;p=p->next);
			p->next=newnode;
			p=newnode;
		}
    }
}

void display(){
	if(head==NULL){
		printf("list is empty");
	}
	else{
		for(p=head;p!=NULL;p=p->next)
		printf("%d->",p->data);
	}
}

void sll_insert_at_begin(){
	int ele;
	printf("emnter the element:");
	scanf("%d",&ele);
	newnode=(struct node*)malloc(sizeof(struct node));
	newnode->data=ele;
	newnode->next=NULL;
	p=head;
	head=newnode;
	newnode->next=p;
	p=newnode;
	
}

void sll_insert_at_end(){
	int ele;
	printf("emnter the element:");
	scanf("%d",&ele);
	newnode=(struct node*)malloc(sizeof(struct node));
	newnode->data=ele;
	newnode->next=NULL;
	for(p=head;p->next!=NULL;p=p->next);
	p->next=newnode;
	p=newnode;
	
	
}

void sll_insert_at_anyposition(){
	 int ele,i,pos=4;
	 printf("enter the element:");
	 scanf("%d",&ele);
	 newnode=(struct node*)malloc(sizeof(struct node));
	 newnode->data=ele;
	 for(p=head,i=1;i<pos;i++,p=p->next)
	 t=p;
	 t->next=newnode;
	 newnode->next=p;
}

void sll_delete_at_begin(){
	p=head;
	head=p->next;
	free(p);
}
void sll_delete_at_end(){
	for(p=head;p->next!=NULL;p=p->next)
	t=p;
	t->next=NULL;
	free(p);
}
void sll_delete_at_anyposition(){
	int i,pos=3;
	for(p=head,i=1;i<pos;p=p->next,i++)
	t=p;
	t->next=p->next;
	free(p);
}
int main(){
    int cho;
	do
	{
		printf("\n**menu**\n");
		printf("\n1.create\n2.display\n3.sll_insert_at_begin\n4.sll_insert_at_end\n5.sll_insert_at_anyposition\n6.sll_delete_at_begin\n7.sll_delete_at_end\n8.sll_delete_at_anyposition\n9.exit\n");
		printf("enter the choice:");
		scanf("%d",&cho);
		
		switch(cho)
		{
			case 1:create();break;
			case 2:display();break;
			case 3:sll_insert_at_begin();break;
			case 4:sll_insert_at_end();break;
			case 5:sll_insert_at_anyposition();break;
            case 6:sll_delete_at_begin();break;
            case 7:sll_delete_at_end();break;
            case 8:sll_delete_at_anyposition();break;
			case 9:exit(0);
			default:printf("enter the no b/w 1 to 9:");
		}
	}while(cho>0 && cho<=9);
	
	return 0;
}
