# CodeWars Java Solutions

---

## Find Nearest square number

Your task is to find the nearest square number, nearest_sq(n) or nearestSq(n), of a positive integer n.

For example, if n = 111, then nearest\_sq(n) (nearestSq(n)) equals 121, since 111 is closer to 121, the square of 11, than 100, the square of 10.

If the n is already the perfect square (e.g. n = 144, n = 81, etc.), you need to just return n.

Good luck :)

Check my other katas:

Alphabetically ordered

Case-sensitive!

Not prime numbers

Find your caterer





---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;

public class NearestSqTest {
    @Test
    public void basicTests() {
        assertEquals(1, CodeWarsMath.nearestSq(1));
        assertEquals(1, CodeWarsMath.nearestSq(2));
        assertEquals(9, CodeWarsMath.nearestSq(10));
        assertEquals(121, CodeWarsMath.nearestSq(111));
        assertEquals(10000, CodeWarsMath.nearestSq(9999));
    }
}
```

---

### Solution

```Java
public class CodeWarsMath {
    public static int nearestSq(final int n){
        int sqrt = (int) Math.sqrt(n);

        int lowerSquare = sqrt * sqrt;
        int upperSquare = (sqrt + 1) * (sqrt + 1);

        if (Math.abs(n - lowerSquare) <= Math.abs(n - upperSquare)) {
            return lowerSquare;
        } else {
            return upperSquare;
        }
    }
}
```
```Java
public class CodeWarsMath {
    public static int nearestSq(final int n){
        return (int) Math.pow(Math.round(Math.sqrt(n)),2);
    }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/5a805d8cafa10f8b930005ba/train/java)