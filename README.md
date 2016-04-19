# C-How-To-Program-Solutions

/* Exercise 4.10 Solution */
#include <stdio.h>

int main( void )
{ 
   int value; /* current value */
   int count = 0; /* number of values */
   int total = 0; /* sum of integers */

   /* display prompt */
   printf( "Enter an integer ( 9999 to end ): " );
   scanf( "%d", &value );

   /* loop while sentinel value not read from user */
   while ( value != 9999 ) { 
      total += value; /* update total */
      ++count;

      /* get next value */
      printf( "Enter next integer ( 9999 to end ): " );
      scanf( "%d", &value );
   } /* end while */

   /* show average if more than 0 values entered */
   if ( count != 0 ) {
      printf( "\nThe average is:  %.2f\n", ( double ) total / count );
   } /* end if */
   else {
      printf( "\nNo values were entered.\n" );
   } /* end else */

   return 0; /* indicate successful termination */
} /* end main */
