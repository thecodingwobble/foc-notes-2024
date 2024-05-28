Data is stored in a string of bits, represented by 1 or 0 (binary)
ASCII system stores 127 bits, not enough for non english
Use
Binary is a <strong>base 2 system</strong>
Denary (most commonly used number system) is a <strong>base 10 system</strong>
Each new digit is a square of 2
⁰ ¹ ² ³ ⁴ ⁵ ⁶ ⁷ ⁸ ⁹

| 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2⁷  | 2⁶  | 2⁵  | 2⁴  | 2³  | 2²  | 2¹  | 2⁰  |
<h3>Decimal to binary</h3>
let the number, n be divided by 2
log the remainder into an array
divide until the quotient is 0
Here is a script to help with that
<code>function toBin(int) {

       let result = "";

       while (int !== 0) {

           if (int % 2 == 1) {

               result += "1";

           } else {

               result += "0";

           }

           int = Math.floor(int / 2);

       }

       return result;

}</code>
<h2>Unsigned integers</h2>
- Only can represent positive numbers
- Used for memory addresses, filesystem & Process identifiers
<h2>Hexadecimal</h2>
Hexadecimal (hex) is a base 16 system
Often used for readability
Often denoted by a <code>0x</code> in front, <font color="#00ff00">or as \x[int]</font>
<h6>Digits in hex:</h6>
0123456789ABCDEF
<h4>Binary to hex</h4>
Check if amount of bits is divisable by 4, if not, pad with 0 until seperatable into 4 bits
<h2>Signed integers</h2>
Leftmost bit is used to identify sign
- 0 for positive
- 1 for negative
Represented by
- Sign and magnitude
- 1's complement
- 2's complement
<h5>Sign and magnitude</h5>
negative values represented by changing Most significant bit (4th bit/leftmost bit)
<h5>1's complement</h5>
negative values are obtained by complementing each bit of the corresponding positive number
-0 is represented by <code>1111</code>
<h5>2's complement</h5>
obtained by forming bit complement of number, then add 1
<strong>There is no -0</strong>
2's complement is used in modern computers as its most efficient in carrying out addition & subtraction
<h6>Truth table for ADD operation</h6>

| a   | b   | result |
| --- | --- | ------ |
| 0   | 0   | 0      |
| 0   | 1   | 1      |
| 1   | 0   | 1      |
| 1   | 1   | 10     |
<h5>Overflow</h5>
Overflow occurs when answer does not fit into number range 
Range = -2ⁿ⁻¹ to +2ⁿ⁻¹-1
4 bits: -8 to 7, 8 bits: -128 127
If 2 Two's complements are added & have same sign; overflow occurs if result has negative sign
Overflow never occurs when adding with different signs 
+n + +n = +n
-n + -n = -n
Overflow occurs:
(+A)+(+B) = (-C)
(-A)+(-B) = (+C)
