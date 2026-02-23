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
```

# 💎 The "Types" of Java

In the Java ecosystem, "Types" can refer to the **Data Types** used in coding or the **Platform Editions** used for different industries.

---

## 1. Data Types (The Building Blocks)
Java is **Statically Typed**, meaning every variable must have a declared type. These are split into two categories:

### A. Primitive Data Types
These are the basic, built-in types that store simple values. They are not objects.

| Type | Size | Description | Example |
| :--- | :--- | :--- | :--- |
| `int` | 4 bytes | Whole numbers | `int age = 25;` |
| `double` | 8 bytes | Fractional numbers | `double price = 19.99;` |
| `char` | 2 bytes | Single character/ASCII | `char grade = 'A';` |
| `boolean`| 1 bit | True or False | `boolean isJavaFun = true;` |

### B. Non-Primitive (Reference) Types
These refer to **Objects**. They are more complex and provide methods to manipulate data.
* **String:** To store text (`String name = "Gemini";`).
* **Arrays:** To store multiple values of the same type.
* **Classes:** User-defined types.



---

## 2. Java Platform Editions
Depending on what you are building (a phone app vs. a huge server), you use a different "flavor" of Java.

### ☕ Java SE (Standard Edition)
The core Java programming platform. It contains all the libraries every Java developer needs (java.lang, java.util, etc.).
* **Use Case:** Desktop apps, basic logic, learning Java.

### 🏢 Java EE / Jakarta EE (Enterprise Edition)
Built on top of SE. It adds features for large-scale, multi-tiered, scalable, and secure network applications.
* **Use Case:** Banking systems, E-commerce websites, Server-side API.

### 📱 Java ME (Micro Edition)
A stripped-down version of Java for devices with limited resources (small memory, low power).
* **Use Case:** Set-top boxes, old mobile phones, embedded sensors.

### 🚀 Java FX
A graph-based framework for creating rich internet applications with modern GUIs.
* **Use Case:** Modern desktop software with high-end graphics.

---

## 3. Variable Scope Types
Where a variable "lives" inside your code also defines its type:

1. **Local Variables:** Declared inside a method. Only usable in that method.
2. **Instance Variables:** Declared inside a class but outside a method. Tied to a specific object.
3. **Static Variables:** Declared with the `static` keyword. They belong to the class itself, not any single object.


#4 🧠 Java Memory: Stack vs. Heap

In Java, the **JVM (Java Virtual Machine)** manages memory using two distinct areas. Understanding the difference is the key to writing efficient code and avoiding memory leaks.

---

## 1. The Stack Memory (The "To-Do" List)
The Stack is used for **method execution** and the storage of local variables.

* **Structure:** Follows **LIFO** (Last-In-First-Out). Like a stack of plates; the last one you put on is the first one you take off.
* **What it stores:** * Primitive types (`int`, `char`, `double`, etc.).
    * The **reference** (memory address) of objects stored in the Heap.
* **Speed:** Extremely fast access.
* **Management:** Automatically managed. When a method finishes, its "stack frame" is deleted instantly.

---

## 2. The Heap Memory (The "Storage Room")
The Heap is a large pool of memory used for **dynamic allocation**.

* **Structure:** No particular order; objects are scattered wherever there is space.
* **What it stores:** All **Objects** (e.g., `String`, `Scanner`, `ArrayList`) and class instances.
* **Speed:** Slower than the stack (requires searching for space and managing pointers).
* **Management:** Managed by the **Garbage Collector (GC)**.
* **Sharing:** Global. All parts of the program can see objects in the Heap if they have the reference.

---

## 🛠️ Visualizing the Process

Imagine this code:
```java
void startApp() {
    int version = 12;            // Primitive
    String name = "Java App";    // Object Reference
}
```
#5 🗑️ Java Garbage Collection (GC) Fast Facts

* **Purpose:** Automatically reclaim Heap memory by deleting unused objects.
* **Trigger:** The JVM triggers GC when it feels memory is running low.
* **Manual Control:** You *cannot* force GC. You can "suggest" it using `System.gc()`, but the JVM might ignore you.
* **The Cost:** GC takes a tiny amount of CPU power. Occasionally, it causes a "Stop-the-World" event where the app pauses for a few milliseconds to clean up.

### The Lifecycle of an Object
1. **Creation:** Object is placed in the Young Generation.
2. **Usage:** The program uses the object via a reference.
3. **Abandonment:** The reference is set to `null` or goes out of scope.
4. **Collection:** The GC identifies the object is unreachable and wipes it out.
