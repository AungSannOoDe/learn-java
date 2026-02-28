# 📘 Java Arrays & ArrayList -- Quick Guide

In Java, **arrays** are objects that store multiple values of the same
type in a single variable.\
Unlike Strings, arrays have a **fixed length** once created.

To manipulate arrays effectively, you will mostly use the built-in
`java.util.Arrays` class.

------------------------------------------------------------------------

## 1️⃣ Basic Array Properties

These are built directly into the array object.

-   **`.length`**\
    Arrays use a property called `length` (not a method).\
    Example:

``` java
int[] numbers = {1, 2, 3};
System.out.println(numbers.length); // 3
```

⚠️ Note: Strings use `.length()` (method), arrays use `.length`
(property).

------------------------------------------------------------------------

## 2️⃣ The `java.util.Arrays` Utility Class

To use this class:

``` java
import java.util.Arrays;
```

### Useful Methods

-   **`Arrays.toString(array)`**\
    Converts array into a readable format.

``` java
System.out.println(Arrays.toString(numbers));
// Output: [1, 2, 3]
```

If you print directly:

``` java
System.out.println(numbers);
```

You'll see something like:

    [I@15db9742

------------------------------------------------------------------------

-   **`Arrays.sort(array)`**\
    Sorts array in ascending order.

``` java
Arrays.sort(numbers);
```

------------------------------------------------------------------------

-   **`Arrays.fill(array, value)`**\
    Fills every slot with the same value.

``` java
Arrays.fill(numbers, 0);
```

------------------------------------------------------------------------

-   **`Arrays.copyOf(original, newLength)`**\
    Creates a new array with a different size.

``` java
int[] bigger = Arrays.copyOf(numbers, 5);
```

------------------------------------------------------------------------

-   **`Arrays.binarySearch(array, key)`**\
    Searches for a value (array must be sorted first).

``` java
int index = Arrays.binarySearch(numbers, 2);
```

------------------------------------------------------------------------

# 🚀 ArrayList (Used in Professional Development)

In real-world Java development, **ArrayList** is used much more often
than regular arrays.

Think of it like this:

-   Array = Fixed-size egg carton 🥚\
-   ArrayList = Magic bag that grows 🎒

To use:

``` java
import java.util.ArrayList;
```

------------------------------------------------------------------------

## Why Use ArrayList?

### ✅ 1. Dynamic Resizing

You don't need to know the size in advance.

``` java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
```

If you add more items, Java automatically increases capacity.

------------------------------------------------------------------------

### ✅ 2. Built-in Methods

-   `.add(value)`
-   `.contains(value)`
-   `.indexOf(value)`
-   `.remove(value)`
-   `.clear()`
-   `.size()`

Example:

``` java
System.out.println(list.contains("Java")); // true
```

------------------------------------------------------------------------

### ✅ 3. Easy Removal

If you remove an item in the middle:

``` java
list.remove("Java");
```

The list automatically shifts elements to fill the gap.

------------------------------------------------------------------------

# 🧠 Summary

  Feature            Array       ArrayList
  ------------------ ----------- -------------
  Fixed Size         ✅ Yes      ❌ No
  Dynamic Resize     ❌ No       ✅ Yes
  Built-in Methods   Limited     Many
  Used in Industry   Sometimes   Very Common

------------------------------------------------------------------------

💡 As an intern or junior developer, you will use **ArrayList 90% of the
time** in professional Java development.
