//perror example 1
#include <stdio.h>
 
int main(void)
{
    FILE *f = fopen("non_existent", "r");  //opening a file which is not existing
    if (f == NULL) 
	{
        perror("fopen() failed");
    } 
	else 
	{
        fclose(f);
    }
}
/*Output:
fopen() failed: No such file or directory
*/