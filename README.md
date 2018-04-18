# barrelfptcol
 Bar Chart - 3-24
BAR CHART – REFERENCE VARIABLES AND POINTERS - C++

This program will show pass by reference variables to functions where the variables will change.  It will show pass by value to functions where the variables will not change.  It will show an array’s constant address passed to a pointer variable in a function that will have the pointer increment through the array by comparing addresses and assign values into the array one by one.  

Create a program to create a horizontal bar chart of three bars made up of three different symbols.  The lengths of the bars will be determined by random numbers (so it will be like a contest to see which symbol has the longest bar in the chart).  It will use a main function and two user defined functions.  One function will use reference variables and the other function will use two pass by value and a character pointer pointing to a character array.  The output will look something like (the ~ won!):

21 30 23					// print three random integer variables in main

@@@@@@@@@@@@@@@@@@@@@			// first character array of first number 21 @
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~	// second character array of second number 30 ~
;;;;;;;;;;;;;;;;;;;;;;;		// third character array of third number 23 ;

main – 
Three integer variables will be declared for the length of the three bars.  Three character arrays of up to size thirty will be declared to hold the cstring made up of the multiple character symbols in the array.  

The refrandom function (see below) will be called and the three integers will be passed as reference variables (not pointers) with a void return.  The refrandom function will assign random numbers to the three variables in the same function, so a pass by reference variables is used.  

In main, the three integer variables will then be printed to show they received values by reference (see above output example).

The pointfill function (see below) will then be called, to fill up the first character array, with three arguments - the value of the first integer variable (the length of the first bar will not change so pass by value), the character @ value (the symbol to draw the first bar out of will not change so pass by value), and the address of the first character array (to fill it up with the first integer number of @ symbols and the array will change so pass the constant pointer address of the array into a pointer variable).  

The pointfill function will be called a second time with the second integer variable, the character ~, and the address of the second character array.  The pointfill will be called a third time with the third integer variable, the character ;, and the address of the third character array.

In main, the first character array will then be printed all at once as a cstring (no loop) on a separate line.  The second character array will similarly be printed on the next line and the third character array will similarly be printed on the next line.  It should look like a three line bar chart of the @, ~, and ; (see above output example).  The winner is the bar with the most number of characters.

refrandom – function that will accept three integer reference parameters and since they are reference variables will have a void return.  In the function, the three reference variables will be assigned a random number between 1 and 30.  Since we want to assign all three variables in one function and we can not directly return all three values, we are using reference variables.

pointfill – function parameters - the value of the length of the bar, the value of the character to draw the bar out of, and a variable character pointer that will accept the address of a constant character array.  Because the function knows the address of the array, it is a void return.  This pointer will increment through the array with pointer notation in a while pointer comparison loop (comparing to a limit pointer holding the ending address of the array, which is the length of the bar spots from the beginning of the array).  As the pointer points at each spot in the array, assign the character argument to where the pointer is pointing (only assigning one character at a time).  When the loop is over, assign a \0 to where the pointer is pointing (to end the cstring).

Submit the program with increased documentation - at least name, exercise, four to five lines about the purpose, and at least 5 lines throughout the program explaining what is going on including some telling what each function does, etc.  

Run your program two times (to show the random results) and save the output (you can copy and paste both runs together into a blank .txt text file).  Make sure your output file is plain text and the up to 30 columns show.  You can add a Utility plain text file to your Resource Files in Visual Studio and paste the Console or you can paste into a plain text editor like TextPad.  Submit both the .cpp program file and the .txt output file.
