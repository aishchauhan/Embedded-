//display 2d array adrress and values
#include<stdio.h>

int main()
{
	int arr[3][4] = {
						{10,11,12,13},
						{20,21,22,23},
						{30,31,32,33}
					};					
	int i,j;
	for(i = 0;i<3;i++)
	{
		printf("Address of %d array = %u %u\n",i,arr[i],*(arr+i));
		for(j = 0;j<4;j++)
		{
			printf("%d ",arr[i][j]);
			printf("%d ",*(*(arr+i)+j));
		}
		printf("\n");
	}
}
/*Output:
Address of 0 array = 6684128 6684128
10 10 11 11 12 12 13 13
Address of 1 array = 6684144 6684144
20 20 21 21 22 22 23 23
Address of 2 array = 6684160 6684160
30 30 31 31 32 32 33 33
*/