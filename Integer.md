# 🔢 The `int` Data Type in Java

The `int` keyword is used to define variables that hold whole numbers. It is a 32-bit signed two's complement integer.

### 📋 Technical Specifications
| Feature | Value |
| :--- | :--- |
| **Size** | 32 bits (4 bytes) |
| **Default Value** | `0` |
| **Minimum Value** | -2,147,483,648 ($-2^{31}$) |
| **Maximum Value** | 2,147,483,647 ($2^{31} - 1$) |

---

### 💻 Code Example: Basic Usage

Here is a simple program showing how to declare, initialize, and perform math with integers.

```java
public class IntegerExample {
    public static void main(String[] args) {
        // 1. Declaration and Initialization
        int speedLimit = 60;
        int currentSpeed = 55;
        
        // 2. Basic Arithmetic
        int speedDifference = speedLimit - currentSpeed;
        
        // 3. Printing the result
        System.out.println("The speed difference is: " + speedDifference + " mph");
        
        // 4. Large Numbers (Using underscores for readability)
        int population = 1_000_000; // The underscores are ignored by Java
        System.out.println("City Population: " + population);
    }
}
