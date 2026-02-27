## The Decision Logic

Think of it like a flow chart:

if: The first door. If the condition is true, enter here.

else if: The "backup" doors. If the first door was locked (false), try this one. You can have as many of these as you need.

else: The "catch-all" door. If none of the above worked, go here.

``` java
if (condition1) {
    // Executes if condition1 is true
} else if (condition2) {
    // Executes if condition1 was false AND condition2 is true
} else {
    // Executes if all previous conditions were false
}
```

``` java
public class GradeCalculator {
    public static void main(String[] args) {
        int score = 85;
        char grade;

        if (score >= 90) {
            grade = 'A';
        } else if (score >= 80) {
            grade = 'B'; // This will execute because 85 >= 80
        } else if (score >= 70) {
            grade = 'C';
        } else if (score >= 60) {
            grade = 'D';
        } else {
            grade = 'F'; // Catch-all for scores below 60
        }

        System.out.println("Your score is " + score + ", so your grade is: " + grade);
    }
}
```
