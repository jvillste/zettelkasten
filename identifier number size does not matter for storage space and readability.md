Because storage size needed to store a number is logarithmic to the size of the number, big identifier numbers do not take much more space than small numbers.

A [[Variable length quantity]] of three bytes can express `(2^7)^3 = 2 097 152` distinct numbers which is enough for most purposes when used for identifying entities. Adding one more byte explodes the space of available numbers to over 200 millions.

Because of this, reading big numbers is also not too difficult especially when using 64 as the base. Here is the same number written in different bases:

- base 10: `16 000 000`
- base 16: `F4 24 00`
- base 64: `9C QA`

Each digit in base 64 encoding encodes six bits. Thus a four digit base 64 encoded number can encode a three byte i.e. 24 bit number with the maximum value of : 16 777 216