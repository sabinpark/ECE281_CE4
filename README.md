ECE281_CE4
==========

Sabin's CE 4

## Program A: *Simple Memory Manipulation*

### Description
Program A loads a value into an accumulator and stores the current value of the accumulator into an address.  This is repeated two more times.

*TARGET PROGRAM END:* 11

*Target met*

### Program
First, the program loads the value of 9h into the accumulator.  From there, the program stores the current value of the accumulator (9h) into a label, *m1*.  *m1* points to the address *B0*.  The program then loads the value of 8h into the accumulator, then stores that value (8h) into a new label, *m2*, which points to the address *C4*.  The same process is repeated for the value of Bh, which is stored into the address, *CB*.  At the end, the program is put into an infinite loop to prevent the program from crashing.



## Program B: *Mathematics*

### Description
Program B retrieves a value from location *B0*, doubles that value, then subtracts that value by 4.  The result is then output to *Port 2*.  

*TARGET PROGRAM END:* 0C

*Target met*

### Program
The program begins by first loading the value of -4 into the accumulator, where -4 is equal to Ch.  Next, the value within address *B0* is added twice to the accumulator.  Finally, the value in the accumulator is output to *Port 2*.  *NOTE:* a positive test value should be in the location of *B0*.  This program also ends with an infinite loop. 

I tested this program with an initial value of 1.  The output was E (-2).  I tested it again with an initial value of 4.  The output was 4.

## Program C: *Loops*

### *UPDATE*
Captain Silva confirmed that this program works.

### Description
Program C reads the value from *Input Port 3*, then displays that value on *Output Port 0*.  *Port 1* displays 1 less of the value from *Port 0*.  *Port 2* displays 1 less of the value from *Port 1*.  From here, *Port 0* will decrement by 1.  Effectively, *Port 1* will decrement so as to be 1 less than the value in *Port 0*, and *Port 2* will also decrement so as to be 1 less than the value in *Port 1*.  Each port will continue to decrement accordingly in an infinite loop.

*TARGET PROGRAM END:* 10

*Target met*

### Program
The program first reads the value from *Input Port 3* and loads that value into the accumulator.  That value is then output into *Port 0*.  The accumulator is then decremented by 1.  The program accomplishes this by adding Fh (-1) to the accumulator.  This current value in the accumulator is then output into *Port 1*.  Again, the accumulator decrements by 1, and then outputs the value into *Port 2*.  From here, the accumulator increments by 1, and the program loops back to outputting the current accumulator value into *Port 0*.  The program will infinitely loop through and decrement each port.

I tested the program by initializing the value of the input to 2.  As expected, Port 0 started with a value of 2, Port 1 became 1, and Port 2 became 0.  The values then decremented accordingly.


## Extra Credit:
Each program matched the target end address for a total of 3 bonus points!
* Program A ends at address 11
* Program B ends at address 0C
* Program C ends at address 10

## Documentation
None.
