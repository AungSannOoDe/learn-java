## Java Bitwise Operators
A comprehensive technical overview of Bitwise and Bit Shift Operators in Java. These operators perform manipulations on individual bits of number types (byte, short, int, and long).

``` java
public class BitwiseDemo {
    public static void main(String[] args) {
        int x = 12; // Binary: 1100
        int y = 10; // Binary: 1010

        // Bitwise AND
        System.out.println("x & y: " + (x & y)); // 8 (Binary: 1000)

        // Bitwise XOR
        System.out.println("x ^ y: " + (x ^ y)); // 6 (Binary: 0110)

        // Bitwise NOT (Inversion)
        System.out.println("~x: " + (~x));       // -13 (Two's Complement)

        // Multiplication by 2 using Left Shift
        int n = 5;
        System.out.println("5 << 1: " + (n << 1)); // 10
    }
}
```
``` java
int red = (color >> 16) & 0xFF;
int green = (color >> 8) & 0xFF;
int blue = color & 0xFF;
```

``` java
int a = 12;  // Binary: 1100
int b = 10;  // Binary: 1010
int result = a & b;  // Binary: 1000 (8 in decimal)

System.out.println("a & b = " + result); // Output: 8
```

 ## Left Shift Operator (<<)
 The Left Shift operator moves all bits in a number to the left by a specified number of positions.
 Logic: For every shift to the left, a 0 is pulled in from the right. The leftmost bits are discarded.Mathematical Effect: Shifting a value $n$ positions to the left is equivalent to:$$\text{result} = \text{value} \times 2^n$$Example: 5 << 2Binary of 5 is 0000 0101.
Shift left by 2 positions.Result: 0001 0100 (which is 20 in decimal).
Calculation: $5 \times 2^2 = 20$.



