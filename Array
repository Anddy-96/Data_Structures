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
 void Addatindex(int x, int y, struct node **a);
 struct node *a = NULL;
 struct node *n = NULL;
 struct node *l = NULL;
 struct node *h = NULL;
 struct node *t = NULL;


 void Addatfirst(int x, struct node **h)
 {
   struct node *nn = (struct node*)malloc(sizeof(struct node));
  nn->x = x;
  nn->y = *h;
  *h = nn;
 }
 void Addatlast(int x, struct node **l)
 {
   struct node *nn = (struct node*)malloc(sizeof(struct node));
   nn->x = x;
   nn->y = NULL;
   (*l)->y = nn;
   *l = nn;
 }
 void removeatlast(struct node **a)
 {
   int i;
   for (i=0;a!=NULL;i++)
   {

   }
 }
 void removeatfirst(struct node **a)
 {

 }
 void removeatindex(struct node **a)
 {

 }
 void removevalue(struct node **a)
 {

 }
 void Getindex(struct node **a)
 {

 }
 void Addatindex(int x, int y, struct node **a)
 {
   t =*a;
   //*h =**a;
   struct node *nn = (struct node*)malloc(sizeof(struct node));
   int i=0;
   while ((*a)!=NULL)
   {
     i=i+1;
     *a = (*a)->y;
   }
   int n=i;
   printf("i value: %d \n",n);
   if(x==1)
   {
     Addatfirst(y, &h);
   }
   if(x==n)
   {
     Addatlast(y, &h);

   }
    printf("t value %d \n",t->x);
    for(i=1;i<=n-1;i++)
    {
      t = t->y;
    }
    nn->x = y;
    nn->y = t->y;
    t->y =nn;
 }
 void printList(struct node *a)
 {
   h=a;
   printf("Your list:\n");
   while(a != NULL)
   { 
     printf("%d\n",a->x);
     a = a->y;
   }
   
   char b;
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
   int c;
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
      printList(h);
      break;
    case 4:
      removeatlast(&h);
      break;
    case 5:
      removeatfirst(&h);
      break;
    case 6:
      removeatindex(&h);
      break;
    case 7:
      removevalue(&h);
      break;
    case 8:
      Getindex(&h);
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
