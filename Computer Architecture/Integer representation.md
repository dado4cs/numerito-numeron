## Unsigned
Use [[Binary system|binary numbers]] to directly represent non-negative integers.
$$
11101_2 = 29
$$
n-bit unsigned number:
- Range: $[ 0, 2^n - 1]$
Standard binary addition and subtraction work for these numbers. 

## Sign/magnitude
A N-bit sign/magnitude number uses the [[Binary system|most significant bit]] (MSB) as the sign and the remaining N-1 bits as the magnitude (absolute value). A sign bit of 0 indicates positive, and a sign bit of 1 indicates negative.
Unfortunately, ordinary binary addition does not work for sign/magnitude numbers. 
n-bit sign-magnitude number:
- Range: $[-(2^{n-1}-1), 2^{n-1}-1]$
This representation has two zeros: $1000\dots000$ and $0000\dots000$ (-0 and +0).

## Two's complement
Two's complement numbers are identical to unsigned numbers except that the most significant bit position has a weight of $-2^{N-1}$ instead of $2^{N-1}$. They overcome the shortcomings of sign/magnitude numbers: zero has a single representation, and ordinary addition works. 
- Range: $[-2^{n-1}, 2^{n-1}-1]$.
The positive numbers have 0 in the most significant position, and negative numbers have a 1 in this position.
A two’s complement number's sign can be reversed in a process called "taking the two’s complement." The process consists of inverting all the bits in the number, then adding 1 to the least significant bit position. This is useful for finding the representation of a negative number or determining the magnitude of a negative number. 
