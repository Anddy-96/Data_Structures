#include <stdio.h>
#include <stdlib.h>
 struct node
 {
  int x;
  struct node *y;
 };
 void Choose(struct node *h);
 void Addatfirst(int x, struct node **h);
 void printList(struct node *a);
 void Addatlast(int x, struct node **l);
 void Addatindex(int x, int z, struct node **a);
 void removeatlast(struct node *a);
 struct node *a = NULL;
 struct node *n = NULL;
 struct node *l = NULL;
 struct node *h = NULL;
 struct node *t = NULL;


 void Addatfirst(int x, struct node **h)
 {
   //printf("2stcheck value: %d\n",(*h)->x);
  struct node *nn = (struct node*)malloc(sizeof(struct node));
  nn->x = x;
  nn->y = *h;
  *h = nn;
  //printf("3stcheck value: %d\n",(*h)->x);
 }
 void Addatlast(int x, struct node **l)
 {

   struct node *nn = (struct node*)malloc(sizeof(struct node));
   nn->x = x;
   nn->y = NULL;
   (*l)->y = nn;
   *l = nn;
 }
 void removeatlast(struct node *a)
 {
   int n=0;
   int i;
   t = a;
   //h = a;
   while(a!=NULL)
   {
        n=n+1;
        a = a->y;
   }
   //printf("1 i:%d\n",i);
   for(i=1;i<n-1;i++)
   {
       t=t->y;
   }
   t->y = NULL;
 }
 void removeatfirst(struct node **a)
 {
    *a=(*a)->y;
    h=*a;
 }
 void removeatindex(int q, struct node **a)
 {
   t =*a;
   struct node *prev = NULL;
   prev = *a;

   int i;

    for(i=1;i<=q-1;i++)
     {
        t = t->y;
     }
     for(i=1;i<q-1;i++)
     {
        prev = prev->y;
     }
    prev->y = t->y;


 }
 void removevalue(int q, struct node *a)
 {
     h = a;
     t = a;

     struct node *prev = NULL;
    prev = a;

     int i=1;
     int n;
    while(a != NULL)
   {
     if(a->x == q)
     {
         //printf("Index of your value is: %d\n",i);
         n=i;
     }
     i=i+1;
     a = a->y;
   }

   printf("n:%d",n);

    for(i=1;i<=n-1;i++)
     {
        t = t->y;
     }
     for(i=1;i<n-1;i++)
     {
        prev = prev->y;
     }
    prev->y = t->y;


 }
 void Getindex(int q, struct node *a)
 {
     int i=1;
    while(a != NULL)
   {
     if(a->x == q)
     {
         printf("Index of your value is: %d\n",i);
     }
     i=i+1;
     a = a->y;
   }
 }
 void Addatindex(int q, int w, struct node **a)
 {
   t =*a;
   struct node *nn = (struct node*)malloc(sizeof(struct node));
   int i;

    for(i=1;i<q-1;i++)
     {
        t = t->y;
     }
     nn->x = w;
     nn->y = t->y;
     t->y =nn;

 }
 void printList(struct node *a)
 {
   //
   t=a;
   printf("Your list:\n");
   while(a != NULL)
   {
     printf("%d\n",a->x);
     a = a->y;
   }

   char b;
   h=t;
   printf("you want to continue y/n :\n");
   scanf("%s",&b);
   if (b == 'y')
   {
      Choose(h);
   }
   else
   {
      printf("Thank you!\n");
   }
 }
 void Choose(struct node *h)
 {
   printf("\nSelect the operations:\n");
   printf("\t1.Add at Last.\n\t2.Add at Beginning.\n\t3.Add at particular index.\n\t4.Remove last.\n\t5.Remove First.\n\t6.Remove at particular index\n\t7.Remove value.\n\t8.Get Index of particular value\n\t9.Display\n");
   int a;
   int b;
   int c,d;
   scanf("%d",&a);
   switch(a)
   {
     case 1:
      printf("Enter the element you want to add:\n");
      scanf("%d",&b);
      Addatlast(b,&l);
      printList(h);
      break;
    case 2:
      printf("Enter the element you want to add:\n");
      scanf("%d",&b);
      Addatfirst(b,&h);
      printList(h);
      break;
    case 3:
      printf("Enter the index where you want to add:\n");
      scanf("%d",&c);
      printf("Enter the element:\n");
      scanf("%d",&b);
      Addatindex(c,b,&h);
      printf("it's been added, select Display option and check\n");
      printList(h);
      break;
    case 4:
      removeatlast(h);
      printList(h);
      break;
    case 5:
      removeatfirst(&h);
      printList(h);
      break;
    case 6:
      printf("Enter the index which you want to remove\n");
      scanf("%d",&c);
      removeatindex(c,&h);
      printList(h);
      break;
    case 7:
      printf("Enter the value which you want to remove\n");
      scanf("%d",&c);
      removevalue(c,h);
      printList(h);
      break;
    case 8:
      printf("Enter the value:\n");
      scanf("%d",&c);
      Getindex(c,h);
      printList(h);
      break;
    case 9:
      printList(h);
      break;
   }

 }
int main(void) {
  int r;
  l = (struct node*)malloc(sizeof(struct node));
  h = (struct node*)malloc(sizeof(struct node));
  a = (struct node*)malloc(sizeof(struct node));
  t = (struct node*)malloc(sizeof(struct node));
  printf("Select:\n\t1.Use Default Link List\n\t2.Make your own Link List\n");
  scanf("%d",&r);
  if(r == 1)
  {
    h->x = 9;
    l->x = 10;
    h->y = l;
    l->y = NULL;
    //Addatfirst(5,&h);
    //Addatlast(11,&l);
    printf("This is your default link List:\n");
    printList(h);
  }
  else
  {
    printf("Enter the number of nodes you want in linklist:\n");
    int i,b;
    scanf("%d",&b);
    n = (struct node *)malloc(b * sizeof(struct node));
    int z;
    for(i=0;i<b;i++)
    {
      printf("Enter node %d value:\n",i+1);
      scanf(" %d", &z);
      (n+i)->x = z;
      if(i>0)
      {
        (n+i-1)->y = (n+i);
      }
    }
    (n+b-1)->y = NULL;
    l = (n+b-1);
    h->x = n->x;
    if(b == 1)
    {
      h->y = NULL;
    }
    else
    {
      h->y = n+1;
    }
    printf("\nDisplying your link list:\n");
    printList(h);
  }
  return 0;
}
