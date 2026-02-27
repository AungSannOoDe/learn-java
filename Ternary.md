
## Ternary Operator
The Ternary Operator in Java is a concise, one-line alternative to a simple if-else statement. 
It is the only operator in Java that takes three operands, which is why it's called "ternary."

$$condition\ ?\ expressionTrue\ :\ expressionFalse;$$

Condition: A boolean expression that evaluates to true or false.

?: The "question" (evaluates the condition).

ExpressionTrue: The value assigned/returned if the condition is true.

:: The "else" separator.

ExpressionFalse: The value assigned/returned if the condition is false.

``` java
int speed = 80;
String status;

if (speed > 60) {
    status = "Fast";
} else {
    status = "Slow";
}
```

``` java
int speed = 80;
String status = (speed > 60) ? "Fast" : "Slow";
```
