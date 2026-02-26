# 🚦 Java Control Flow Guide

Control flow statements break up the execution flow by employing decision-making, looping, and branching, enabling your program to conditionally execute blocks of code.



---

## 1. Selection Statements (Decision Making)

Selection statements allow your program to choose different paths of execution based on the outcome of an expression.

### 🏁 `if-else` Statement
The most basic control flow statement. It executes a block of code only if a specified condition is true.

```java
int score = 85;

if (score >= 90) {
    System.out.println("Grade: A");
} else if (score >= 80) {
    System.out.println("Grade: B"); // This will execute
} else {
    System.out.println("Grade: C");
}
```
```java
String day = "WEDNESDAY";

switch (day) {
    case "MONDAY":
        System.out.println("Start of the week!");
        break;
    case "WEDNESDAY":
        System.out.println("Hump day!");
        break;
    default:
        System.out.println("Just another day.");
}
```
