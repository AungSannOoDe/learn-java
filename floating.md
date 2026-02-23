# 🌊 Float vs. Double in Java

While both types store decimal numbers, they differ in **precision** (how many digits they can hold accurately) and **memory consumption**.

### 📊 Key Differences Table

| Feature | `float` | `double` (Default) |
| :--- | :--- | :--- |
| **Size** | 32-bit (4 bytes) | 64-bit (8 bytes) |
| **Precision** | ~6-7 decimal digits | ~15-16 decimal digits |
| **Suffix** | Must end with `f` or `F` | Optional `d` or `D` |
| **Memory** | Efficient for large arrays | Uses more RAM |



---

### 💻 Code Example: Precision Test

This example shows why `double` is the industry standard for most calculations.

```java
public class DecimalExample {
    public static void main(String[] args) {
        // Declaration
        // Note: You MUST add 'f' to a float, otherwise Java thinks it's a double
        float myFloat = 3.1415926535f; 
        double myDouble = 3.141592653589793;

        System.out.println("Float value:  " + myFloat);
        System.out.println("Double value: " + myDouble);
    }
}
