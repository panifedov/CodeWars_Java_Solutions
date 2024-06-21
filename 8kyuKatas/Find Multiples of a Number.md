# CodeWars Java Solutions

---

## Find Multiples of a Number

In this simple exercise, you will build a program that takes a value, integer , and returns a list of its multiples up to another value, limit . If limit is a multiple of integer, it should be included as well. There will only ever be positive integers passed into the function, not consisting of 0. The limit will always be higher than the base.

For example, if the parameters passed are (2, 6), the function should return [2, 4, 6] as 2, 4, and 6 are the multiples of 2 up to 6.

```

```


---

### Given Code

```Java

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertArrayEquals;

// TODO: Replace examples and use TDD by writing your own tests

class SolutionTest {
    @Test
    void testExamples() {
        assertArrayEquals(new int[] { 5, 10, 15, 20, 25 }, Multiples.find(5, 25), "Testing for base=5 and limit=25");
        assertArrayEquals(new int[] { 1, 2 }, Multiples.find(1, 2), "Testing for base=1 and limit=2");
        assertArrayEquals(new int[] { 5 }, Multiples.find(5, 7), "Testing for base=5 and limit=7");
        assertArrayEquals(new int[] { 4, 8, 12, 16, 20, 24 }, Multiples.find(4, 27), "Testing for base=4 and limit=27");
        assertArrayEquals(new int[] { 11, 22, 33, 44 }, Multiples.find(11, 54), "Testing for base=11 and limit=54");
    }
}
```

---

### Solution

``` Java
   import java.util.ArrayList;

public class Multiples {
    public static int[] find(int base, int limit) {
        ArrayList<Integer> resultList = new ArrayList<>();

        for(int i = base; i <= limit; i+=base){
            resultList.add(i);
        }

        int[] result = new int[resultList.size()];
        for(int i = 0; i < resultList.size(); i++){
            result[i] = resultList.get(i);
        }

        return result;
        
    }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/58ca658cc0d6401f2700045f/train/java)