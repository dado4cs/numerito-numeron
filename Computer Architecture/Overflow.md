Digital systems usually operate on a fixed number of digits. 
Addition is said to **overflow** if the result is too large to fit in the available bits. 
Adding two N-bit numbers in [[Integer representation|Two's complement]] (either two positive numbers or two negative numbers) may cause overflow if the result is greater than $2^{N-1}-1$ or less than $-2^{N-1}$. 
Overflow occurs if the carry into the MSB is different from the carry out of the MSB.
