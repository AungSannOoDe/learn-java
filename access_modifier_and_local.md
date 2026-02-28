# 📘 Java Variable Scope & Access Modifiers

## 1️⃣ Variable Scope in Java

Variable scope defines **where a variable can be accessed** in your program.

### 1. Local Variables (Method Scope)
- Declared inside a method or block
- Only accessible within that method/block
- Must be initialized before use

```java
public class Example {
    public static void main(String[] args) {
        int number = 10;  // local variable
        System.out.println(number);
    }
}
```

### 2. Instance Variables (Object Scope)
- Declared inside a class but outside any method
- Each object has its own copy
- Gets default values (0, null, false)

```java
public class Student {
    String name;
    int age;

    void display() {
        System.out.println(name + " is " + age + " years old.");
    }
}

Student s1 = new Student();
s1.name = "Alice";
s1.age = 20;
s1.display();
```

### 3. Static Variables (Class Scope)
- Belongs to the class, not objects
- Shared among all objects
- Only one copy exists

```java
public class Counter {
    static int count = 0;

    Counter() {
        count++;
    }
}

Counter c1 = new Counter();
Counter c2 = new Counter();
System.out.println(Counter.count);  // Output: 2
```

### 4. Block Scope
- Declared inside `{ }`
- Only exists within that block

```java
if (true) {
    int x = 5;
    System.out.println(x);
}
// System.out.println(x); ❌ ERROR
```

### Scope Table
| Type | Declared Where | Lifetime | Shared? |
|------|----------------|----------|---------|
| Local | Method/block | Method execution | ❌ No |
| Instance | Class | Object lifetime | ❌ No |
| Static | Class (static) | Program lifetime | ✅ Yes |

---

## 2️⃣ Access Modifiers – Public & Private

### Public
- Accessible from **anywhere**
- Often used for methods or classes meant to be global

```java
public class Person {
    public String name;
    public void display() {
        System.out.println(name);
    }
}

Person p = new Person();
p.name = "Alice";
p.display();
```

### Private
- Accessible **only within the same class**
- Used for **data hiding**
- Accessed through **getter/setter** methods

```java
public class Person {
    private String name;

    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
}

Person p = new Person();
p.setName("Alice");
System.out.println(p.getName());
// System.out.println(p.name); ❌ ERROR
```

### Quick Comparison
| Modifier | Visible From | Example Use |
|----------|--------------|-------------|
| public   | Anywhere     | API methods |
| private  | Same class   | Sensitive data |

### Example Combining Both
```java
public class BankAccount {
    private double balance;

    public void deposit(double amount) {
        if (amount > 0) balance += amount;
    }

    public double getBalance() {
        return balance;
    }
}

BankAccount account = new BankAccount();
account.deposit(500);
System.out.println(account.getBalance());
// account.balance = 1000; ❌ ERROR
```

