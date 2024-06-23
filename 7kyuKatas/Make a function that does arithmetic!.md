# CodeWars Java Solutions

---

## Make a function that does arithmetic!


Given two numbers and an arithmetic operator (the name of it, as a string), return the result of the two numbers having that operator used on them.

a and b will both be positive integers, and a will always be the first number in the operation, and b always the second.

The four operators are "add", "subtract", "divide", "multiply".


```
5, 2, "add"      --> 7
5, 2, "subtract" --> 3
5, 2, "multiply" --> 10
5, 2, "divide"   --> 2.5
```




---

### Given Code

```Java
Sample Tests
        1
import org.junit.Test;
2
import static org.junit.Assert.assertEquals;
3
import org.junit.runners.JUnit4;
4
        ​
        5
// TODO: Replace examples and use TDD development by writing your own tests
        6
        ​
        7
public class SolutionTest {
8
    @Test
9
    public void testBasic() {
        10
        assertEquals("'add' should return the two numbers added together!", 3, ArithmeticFunction.arithmetic(1, 2, "add"));
        11
        assertEquals("'subtract' should return a minus b!", 6, ArithmeticFunction.arithmetic(8, 2, "subtract"));
        12
        assertEquals("'multiply' should return a multiplied by b!", 10, ArithmeticFunction.arithmetic(5, 2, "multiply"));
        13
        assertEquals("'divide' should return a divided by b!", 4, ArithmeticFunction.arithmetic(8, 2, "divide"));
        14
    }
15
}
```

---

### Solution


```Java
class ArithmeticFunction {
    public static int arithmetic(int a, int b, String operator) {
        switch (operator) {
            case "add":
                return a + b;
            case "subtract":
                return a - b;
            case "multiply":
                return a * b;
            case "divide":
                return a / b;
            default:
                throw new IllegalArgumentException("Unknown operator: " + operator);
        }
    }
}
```



[See on CodeWars.com](https://www.codewars.com/kata/583f158ea20cfcbeb400000a/train/java)