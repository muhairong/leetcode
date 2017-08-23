## two's-complement
- An N-bit two's-complement numeral system can represent every integer in the range −(2N − 1) to +(2N − 1 − 1)
- In two's complement notation, a non-negative number is represented by its ordinary binary representation; in this case, the most significant bit is 0. Though, the range of numbers represented is not the same as with unsigned binary numbers. For example, an 8-bit unsigned number can represent the values 0 to 255 (11111111). However a two's complement 8-bit number can only represent positive integers from 0 to 127 (01111111), because the rest of the bit combinations with the most significant bit as '1' represent the negative integers −1 to −128.
  -  the most significant bit is 0 when it is a possitive number, while 1 when it is a negative number
- To get the two's complement of a binary number, the bits are inverted, or "flipped", by using the bitwise NOT operation; the value of 1 is then added to the resulting value, ignoring the overflow which occurs when taking the two's complement of 0

### example: 32-bit signed integer
- range: -2^31 ~ 2^31-1
- there are 2^32 integers in total
- the most significant bit is the sign bit: 1 -, 0 +

### INT_MAX and INT_MIN
- INT_MAX: 2^31-1
- INT_MIN: -2^31
- note that INT_MIN can't change to be a positive integer by multiplying -1, because it will overflow! Therefore, in determining the boundary conditions, we must pay special attention to it！
- some equation:
  - INT_MAX + 1 = INT_MIN
  - INT_MIN - 1 = INT_MAX
  - -INT_MIN = INT_MIN
  
### another example:
3 bit integer
- 0 0 0  =  0
- 0 0 1  =  1
- 0 1 0  =  2
- 0 1 1  =  3
- 1 1 1  = -1
- 1 1 0  = -2
- 1 0 1  = -3
- 1 0 0  = -4
