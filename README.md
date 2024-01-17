1. What is the address (in hexadecimal) of the first and last instruction in the loop?
	
	1st: 0x00010534, 2nd: 0x00010560

2. Is the loop of the "while(condition)-do", "repeat-until(condition)", or "do-while(condition)" form?

   do-while(condition)

3. Do the values of 'x' increase or decrease?

   they increase

4. In the form of "b *ADDRESS", what is the command to set a breakpoint on the line where you can observe the new value of 'y' after it is calculated? Actually use "print $r0" to check and make sure the register you think is 'y' has been updated and has the correct value.

   b *0x0001054c

5. What two gdb commands can you enter so that at each and every step, gdb will print both the decimal and hexadecimal form of the value 'y'?

   print/x for hexadecimal values and print/d for decimal values

6. The loop as written only calculates the value of 'y' for the values of 'x' between 0 and 9. It should calculate the value of 'y' for all values of 'x' between 0 and 10. Why does the loop stop at 9 and what change would fix it?

   because the condition uses 'blt', which excludes 10, changing it to 'ble' would be inclusive

7. Correct the code in "loop.s", assemble and step through the program again in gdb. Fill in the following table:

register        register                register
   x               y                       y
(counter)       (decimal)               (hexadecimal)

   0            _____7____              0x7

   1            ____-1____              0xFFFFFFFF

   2            ____-9____              0xFFFFFFF7

   3            ___-17____              0xFFFFFFEF

   4            ___-25____              0xFFFFFFE7

   5            ___-33____              0xFFFFFFDF

   6            ___-41____              0xFFFFFFD7

   7            ___-49____              0xFFFFFFCF

   8            ___-57____              0xFFFFFFC7

   9            ___-65____              0xFFFFFFBF

  10            ___-73____              0xFFFFFFB7
  

=====================
 Octal Dump Questions
=====================

8. What type of data is in the source file?

   it displays each byte of the source code file as an individual character such as \n \t or plaint text characters

9. What type of data is in the executable?

   it displays machine code and binary data

BONUS:

10. Use the directory list command (ls -l) to determine the size of your source file (loop.s) and the executable (loop). How do the files compare in size? Which is bigger? In order to get any credit you must also explain why it is bigger.

   loop.s (1008 bytes), loop (510k bytes). The executable is bigger because it has been linked with other object files and libraries

