/*
4)How the arguments passed or pushed to other function and how it assigns the value to arguments. 
Explain using diagram for below example
*/

int main()
{
int a=10,b=20,c=30;
  while(1)
  {
  	data_acq(a, b, c);
  }
}

void data_acq(int x, int y, int z)
{
	....	
}
/*
Here the "pass by value" method is used to pass value to function data_acq().
In pass by value method the values of actual parmeters a,b and c is copied/passed to formal parameters x,y and z
In stack seperate memory will be allocated for formal parameters whenever the data_acq() is called.
After memory allocation "a" value will be copied to "x", "b" value will be copied to "y" and "c" value will be copied to "z".
*/