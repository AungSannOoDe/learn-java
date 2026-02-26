# ⚖️ Java Relational Operators

Relational operators (also called **Comparison Operators**) are used to compare two values. In Java, these operations always result in a `boolean` value: either `true` or `false`.



---

## 📊 Comparison Table

| Operator | Name | Description | Example ($a=10, b=20$) | Result |
| :---: | :--- | :--- | :--- | :--- |
| `==` | **Equal to** | Returns true if both operands are equal | `a == b` | `false` |
| `!=` | **Not equal to** | Returns true if operands are different | `a != b` | `true` |
| `>` | **Greater than** | True if the left operand is greater than the right | `a > b` | `false` |
| `<` | **Less than** | True if the left operand is less than the right | `a < b` | `true` |
| `>=` | **Greater or equal** | True if the left is greater than or equal to the right | `a >= 10` | `true` |
| `<=` | **Less or equal** | True if the left is less than or equal to the right | `a <= 5` | `false` |

---

## 🔍 Implementation Example

Relational operators are most commonly used inside `if` statements and `while` loops to control the flow of the program.

```java
public class ComparisonDemo {
    public static void main(String[] args) {
        int userAge = 20;
        int minimumAge = 18;

        // Using Greater Than or Equal To
        if (userAge >= minimumAge) {
            System.out.println("Access Granted: You are an adult.");
        } else {
            System.out.println("Access Denied.");
        }

        // Using Not Equal To
        String status = "Inactive";
        if (status != "Active") {
            System.out.println("System is currently offline.");
        }
    }
}
