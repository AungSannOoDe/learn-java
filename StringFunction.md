## Immutable vs mutable
An immutable object cannot be modified after it is created.
``` java
public class Main {
    public static void main(String[] args) {

        String name = "Java";
        name=name.concat(" Programming");

        System.out.println(name);
    }
}
```
A mutable object can be modified without creating a new object.

``` java
public class Main {
    public static void main(String[] args) {

        StringBuilder sb = new StringBuilder("Java");
        sb.append(" Programming");

        System.out.println(sb);
    }
}
```
### Immutable object
"Java"  →  "Java Programming"
(new object created)

### mutable object
Updated Internal


In Java, the `String` class is one of the most powerful tools in your
programming toolkit.

Since **strings are immutable** (cannot be changed once created), all
string methods return a **new String** or a result instead of modifying
the original string.

------------------------------------------------------------------------

## 1️⃣ Comparison & Basic Information

-   **`.equals(String another)`**\
    Compares the actual content of two strings.\
    ⚠️ Never use `==` for content comparison.

-   **`.equalsIgnoreCase(String another)`**\
    Compares content while ignoring uppercase/lowercase differences.

-   **`.length()`**\
    Returns the number of characters in the string.

-   **`.isEmpty()`**\
    Returns `true` if the string length is 0.

------------------------------------------------------------------------

## 2️⃣ Transformation

-   **`.toLowerCase()`**\
    Converts the entire string to lowercase.

-   **`.toUpperCase()`**\
    Converts the entire string to uppercase.

-   **`.trim()`**\
    Removes whitespace from the beginning and the end.

-   **`.replace(char old, char new)`**\
    Replaces all occurrences of a specific character or sequence.

------------------------------------------------------------------------

## 3️⃣ Extraction & Searching

-   **`.charAt(int index)`**\
    Returns the character at a specific position (index starts from 0).

-   **`.substring(int begin, int end)`**\
    Extracts part of the string from `begin` up to (but not including)
    `end`.

-   **`.contains(CharSequence s)`**\
    Checks if a specific word or sequence exists inside the string.

-   **`.indexOf(String s)`**\
    Returns the index of the first occurrence of a character or
    substring.

------------------------------------------------------------------------

## 4️⃣ Splitting & Joining

-   **`.split(String regex)`**\
    Breaks a string into an array based on a separator (like comma or
    space).

-   **`String.join(CharSequence delimiter, Iterable elements)`**\
    Joins multiple strings together using a specified separator.

   ## 🧠 Important Reminder

Because `String` is immutable:

``` java
String name = "Java";
name.toUpperCase();
System.out.println(name);   // Still "Java"
```

To store the changed value:

``` java
name = name.toUpperCase();
``` 






