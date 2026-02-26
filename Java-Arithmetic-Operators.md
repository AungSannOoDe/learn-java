# 🧮 Java Arithmetic Operators

Arithmetic operators are used to perform mathematical operations such as addition, subtraction, multiplication, and division. In Java, these operators work with all primitive numeric types: `byte`, `short`, `int`, `long`, `float`, and `double`.

---

## 1. The Five Basic Operators

Java provides five binary arithmetic operators that require two operands.

| Operator | Name | Description | Example ($a=10, b=3$) | Result |
| :---: | :--- | :--- | :--- | :--- |
| `+` | **Addition** | Adds two values | `a + b` | `13` |
| `-` | **Subtraction** | Subtracts right from left | `a - b` | `7` |
| `*` | **Multiplication** | Multiplies two values | `a * b` | `30` |
| `/` | **Division** | Divides left by right | `a / b` | `3` |
| `%` | **Modulus** | Returns the remainder | `a % b` | `1` |



---

## 2. Deep Dive: Division and Modulus

### 📉 Integer vs. Floating-Point Division
The behavior of the `/` operator depends on the data types of the operands:
* **Integer Division:** If both operands are integers, Java discards the fractional part (it does **not** round).
* **Floating-Point Division:** If at least one operand is a `double` or `float`, Java performs a precise decimal division.

```java
int x = 10 / 3;       // Result: 3
double y = 10.0 / 3;  // Result: 3.3333333333333335
```
## 2.Operator Precedence (Order of Operations)
Multiplication, Division, and Modulus * / % (evaluated Left-to-Right)

Addition and Subtraction + - (evaluated Left-to-Right)

# ⚖️ Java Operator Precedence and Associativity

In Java, **Precedence** determines the order in which operators are evaluated. **Associativity** determines the direction of evaluation (Left-to-Right or Right-to-Left) when operators have the same level of precedence.



---

## 📊 Operator Priority Table

| Priority | Operator | Name | Associativity |
| :--- | :--- | :--- | :--- |
| **1st** | `()` | Parentheses | Left-to-Right |
| **2nd** | `expr++`, `expr--` | Postfix Increment / Decrement | Left-to-Right |
| **3rd** | `++expr`, `--expr`, `+`, `-`, `!` | Prefix Inc/Dec, Unary Plus/Minus, Logical NOT | **Right-to-Left** |
| **4th** | `*`, `/`, `%` | Multiplicative (Multi, Div, Mod) | Left-to-Right |
| **5th** | `+`, `-` | Additive (Add, Sub) | Left-to-Right |
| **6th** | `=`, `+=`, `-=`, `*=`, `/=`, `%=` | Assignment Operators | **Right-to-Left** |

---

## 🔍 Key Concepts

### 1. Precedence (The "Rank")
Higher priority operators are evaluated before lower priority ones.
* **Example:** `10 + 5 * 2`
* Multiplication (`*`) is **4th** priority, while Addition (`+`) is **5th**.
* **Result:** `10 + 10 = 20`.

### 2. Associativity (The "Tie-Breaker")
When two operators have the same priority, associativity tells Java which way to go.

* **Left-to-Right:** Common for math. 
  * `10 / 5 * 2` → `(10 / 5) * 2` = `4`.
* **Right-to-Left:** Common for Assignment and Unary.
  * `a = b = c = 10;` → `a = (b = (c = 10));` (All variables become 10).

---

## 💻 Code Example: Precedence in Action


```java
public class PrecedenceDemo {
    public static void main(String[] args) {
        int a = 10;
        int b = 5;
        int c = 2;

        // 1. Multiplicative before Additive
        int result1 = a + b * c; 
        System.out.println("10 + 5 * 2 = " + result1); // Output: 20

        // 2. Parentheses override everything
        int result2 = (a + b) * c; 
        System.out.println("(10 + 5) * 2 = " + result2); // Output: 30

        // 3. Postfix vs Prefix
        int x = 5;
        System.out.println(x++); // Prints 5 (then becomes 6)
        System.out.println(++x); // Becomes 7 (then prints 7)
    }
}
```
# ⚖️ Java Operator Precedence: The Complete Guide

This table includes all major operators in Java, ranked from **highest priority (1st)** to **lowest priority (14th)**.



---

## 📊 Complete Operator Priority Table

| Priority | Operator | Name | Associativity |
| :--- | :--- | :--- | :--- |
| **1st** | `()` `[]` `.` | Parentheses, Array, Member Access | Left-to-Right |
| **2nd** | `expr++` `expr--` | Postfix Increment/Decrement | Left-to-Right |
| **3rd** | `++expr` `--expr` `+` `-` `!` `~` | Prefix Inc/Dec, Unary, Logical/Bitwise NOT | **Right-to-Left** |
| **4th** | `*` `/` `%` | Multiplicative (Multi, Div, Mod) | Left-to-Right |
| **5th** | `+` `-` | Additive (Add, Sub) | Left-to-Right |
| **6th** | `<<` `>>` `>>>` | Shift Operators (Bitwise) | Left-to-Right |
| **7th** | `<` `>` `Explanation` `>=` `instanceof` | Relational/Comparison | Left-to-Right |
| **8th** | `==` `!=` | Equality | Left-to-Right |
| **9th** | `&` | Bitwise AND | Left-to-Right |
| **10th** | `^` | Bitwise XOR | Left-to-Right |
| **11th** | `|` | Bitwise OR | Left-to-Right |
| **12th** | `&&` | **Logical AND** | Left-to-Right |
| **13th** | `||` | **Logical OR** | Left-to-Right |
| **14th** | `? :` | Ternary Operator | **Right-to-Left** |
| **15th** | `=` `+=` `-=` `*=` `/=` `%=` | Assignment Operators | **Right-to-Left** |

---

## 💡 Important Rules to Remember

### 1. Logical "Short-Circuiting"
In Java, `&&` and `||` are **Short-Circuit** operators. 
* For `&&`: If the first part is `false`, Java doesn't even look at the second part (the whole thing is already false).
* For `||`: If the first part is `true`, Java skips the second part (the whole thing is already true).

### 2. Relational vs. Equality
Comparison operators (`<`, `>`) have higher priority than Equality operators (`==`, `!=`).
* **Example:** `5 + 2 == 7` 
* 1. `5 + 2` is done first (7).
* 2. `7 == 7` is done next (true).

### 3. The Power of Parentheses `()`
Parentheses have the **absolute highest priority**. If you want a specific part of your logic to happen first, wrap it in brackets. It also makes your code much easier for humans to read!

---

## 💻 Complex Example

```java
boolean result = 10 + 5 > 12 && 5 * 2 == 10;
```
