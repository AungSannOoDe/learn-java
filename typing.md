# 🧩 Programming Type Systems

In programming, we categorize languages based on **when** they check types and **how strictly** they enforce the rules. Java is both **Statically Typed** and **Strongly Typed**.

---

## 1. Static vs. Dynamic (The "When")
This describes **when** the computer verifies your variable types.

### 🛡️ Static Typing (Java, C++, Swift)
Types are checked **at Compile-Time** (before the program runs).
* **Requirement:** You must declare the type (e.g., `int x = 10;`).
* **Pros:** Catches bugs early; better performance.
* **Cons:** More verbose (more typing).

### 🏃 Dynamic Typing (Python, JavaScript, Ruby)
Types are checked **at Runtime** (while the program is running).
* **Requirement:** No type declaration needed (e.g., `x = 10`).
* **Pros:** Faster to write; flexible code.
* **Cons:** Errors can hide until the app is in the user's hands.

---

## 2. Strong vs. Weak (The "Rules")
This describes **how strictly** the language handles operations between different types.

### 🧱 Strong Typing (Java, Python)
The language has **Strict Rules**. It will not "guess" what you want to do.
* **Java Example:** `int x = "5" + 2;` ➡️ **CRASH/ERROR**. You must manually convert the String to an Integer.

### 🧶 Weak Typing (JavaScript, C)
The language is **Flexible/Loose**. It performs "Type Coercion" (automatic conversion).
* **JS Example:** `"5" + 2` ➡️ Result: `"52"`. It assumes you want a String and converts the number for you.

---

## Summary Comparison Table

| Language | Type Checking (When) | Rule Strictness (How) |
| :--- | :--- | :--- |
| **Java** | **Static** | **Strong** |
| **Python** | **Dynamic** | **Strong** |
| **JavaScript** | **Dynamic** | **Weak** |
| **C++** | **Static** | **Intermediate** |

---

## 💡 Why Java chose Static & Strong
Java was built for large, mission-critical systems (Banks, Android, Servers). 
1. **Static** ensures that typos are caught by the compiler immediately.
2. **Strong** prevents data corruption from accidental "mixing" of data types.

> **Pro-Tip:** In Java, if you need to turn a `double` into an `int`, you must use **Casting**: 
> `int myInt = (int) 5.99; // Result is 5`
