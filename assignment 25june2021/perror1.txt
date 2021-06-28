//perror example 1
#include <stdio.h>

int main () {
   FILE *fp;

   /* first rename if there is any file */
   rename("file.txt", "newfile.txt");

   /* now let's try to open same file */
   fp = fopen("file.txt", "r");  //trying to open a file which does not exist
   if( fp == NULL ) 
   {
      perror("no file error: ");
      return(-1);
   }
   fclose(fp);
      
   return(0);
}

/*output:
no file error: : No such file or directory
*/