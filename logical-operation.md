### 📝 Logical Operators Summary
* Use `&&` when you need **ALL** conditions to be met.
* Use `||` when you need **ANY** condition to be met.
* Use `!` to check if something is **NOT** the case.

**Precedence Note:** `!` is evaluated first, then `&&`, then `||`.

```java
int balance = 500;
int pinRequest = 1234;
int correctPin = 1234;
int withdrawAmount = 100;

// Both must be true
if (withdrawAmount <= balance && pinRequest == correctPin) {
    System.out.println("Withdrawal Successful!");
} else {
    System.out.println("Invalid PIN or Insufficient Funds.");
}
```
```java
int age = 70;
boolean isStudent = false;

// If either is true, the whole thing is true
if (isStudent || age >= 65) {
    System.out.println("You get the 50% discount!");
} else {
    System.out.println("Regular price applies.");
}
```
```java
boolean isLoggedIn = false;

// If NOT logged in (if !false is true)
if (!isLoggedIn) {
    System.out.println("Please log in to continue.");
}
```
