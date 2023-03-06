#include <iostream>

using namespace std;

int main()
{
   const int N = 10;
   int a [N] = { 8, 2, 4, 6, 7, 5, 3, 9, 1, 0,};
   int min = 0; 
   int buf = 0;
   int i;
   for (i = 0; i < N; i++)
   {
   min = i; 
   for ( int j = i + 1; j < N; j++ )
   min = (a [j] < a [min] ) ? j : min;
   if (i != min)
   {
       buf = a[i];
       a[i] = a[min];
       a[min] = buf;
       
   }
   }   
   for (int i = 0; i < N; i++)
   cout << a[i] << "";
   cout << endl;
   
}
