/*
3.Left rotate an array upto user's choice
*/
#include<stdio.h>
#define ARRAY_SIZE 5

int main()
{
   int numList[ARRAY_SIZE];
   int i=0,j=0,temp,leftRotationNum;
   printf("Enter the %d array element\n",ARRAY_SIZE);
   for(i=0 ; i < ARRAY_SIZE ; i++)
   {
       scanf("%d",&numList[i]);
   }
   printf("Enter the number of time array to be left rotated\n");
   scanf("%d",&leftRotationNum);
   for(j=0 ; j < leftRotationNum; j++)
   {
       temp = numList[0];
       for(i=0 ; i < ARRAY_SIZE-1; i++)
       {
           numList[i] = numList[i+1];
       }
       numList[i]=temp;
   }
   printf("Left rotated number order is\n");
   for(i=0 ; i < ARRAY_SIZE ; i++)
   {
       printf("%d ",numList[i]);
   }
   return 10;
}
/*
Output:
-------------------------------------------------
Test case 1
Enter the 5 array element
1
2
3
4
5
Enter the number of time array to be left rotated
3
Left rotated number order is
4 5 1 2 3
-------------------------------------------------
-------------------------------------------------
Test case 2
Enter the 5 array element
1
2
3
4
5
Enter the number of time array to be left rotated
0
Left rotated number order is
1 2 3 4 5
-------------------------------------------------
*/