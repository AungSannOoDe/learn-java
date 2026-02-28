# 📘 Java Loops – While & Do-While

Loops are used to execute a block of code **multiple times** based on a condition.

---

## 1️⃣ while Loop

The `while` loop **checks the condition first**, then executes the code block.
If the condition is false initially, the loop **may not execute at all**.

### Syntax:
```java
while (condition) {
    // code to execute
}
```

### Example:
```java
public class Main {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println("i = " + i);
            i++;
        }
    }
}
```

**Output:**
```
i = 1
i = 2
i = 3
i = 4
i = 5
```

### Key Points:
- Condition is **checked first**
- Loop may **never execute** if condition is false initially
- Use when **number of iterations is unknown**

---

## 2️⃣ do-while Loop

The `do-while` loop **executes the code block first**, then checks the condition.
This ensures the code block **runs at least once**.

### Syntax:
```java
do {
    // code to execute
} while (condition);
```

### Example:
```java
public class Main {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println("i = " + i);
            i++;
        } while (i <= 5);
    }
}
```

**Output:**
```
i = 1
i = 2
i = 3
i = 4
i = 5
```

### Key Points:
- Executes **at least once**
- Condition is checked **after the loop body**
- Useful when you want the loop to **run once before checking** a condition

---

## 3️⃣ Quick Comparison Table
| Feature        | while               | do-while           |
|----------------|-------------------|------------------|
| Condition Check | Before loop body   | After loop body  |
| Minimum Execution | 0 times          | 1 time           |
| Use Case        | Unknown iterations | Must run once    |

---

## 4️⃣ break & continue Examples

### break Example:
```java
int i = 1;
while (i <= 10) {
    if (i == 5) {
        break;  // exit loop
    }
    System.out.println(i);
    i++;
}
```
**Output:**
```
1
2
3
4
```

### continue Example:
```java
int i = 0;
do {
    i++;
    if (i % 2 == 0) {
        continue;  // skip even numbers
    }
    System.out.println(i);
} while (i < 5);
```
**Output:**
```
1
3
5
```

