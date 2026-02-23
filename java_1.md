# Introduction to Java ☕

Welcome to the world of Java! If you're looking for a language that is reliable, runs almost everywhere, and is the backbone of many massive systems, you've picked the right one.

Java is a **class-based, object-oriented programming language**. Its "secret sauce" is the principle of **Write Once, Run Anywhere (WORA)**.

---

## 1. How Java Works
Unlike some languages that talk directly to your computer's hardware, Java talks to a middleman called the **Java Virtual Machine (JVM)**.

1.  **Source Code:** Write code in a `.java` file.
2.  **Compiler:** Turns code into **Bytecode** (`.class` file).
3.  **JVM:** Executes the bytecode on any device.

---

## 2. Your First "Hello World"
Every Java program starts with a **class**. Here is the standard structure:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
