# CodeWars Java Solutions

---

## Convert to Binary

Task Overview
Given a non-negative integer n, write a function to_binary/ToBinary which returns that number in a binary format.

```
    to_binary(1)  /* should return 1 */
    to_binary(5)  /* should return 101 */
    to_binary(11) /* should return 1011 */
```


---

### Given Code

```Java

import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;


public class KataTest {
    @Test
    public void testToBinary() {
        assertEquals(1, Kata.toBinary(1));
        assertEquals(10, Kata.toBinary(2));
        assertEquals(11, Kata.toBinary(3));
        assertEquals(101, Kata.toBinary(5));
    }
}
```

---

### Solution

``` Java
    public class Kata {
    
        public static int toBinary(int n) {
            if (n == 0) {
                return 0;
            }
    
            StringBuilder binary = new StringBuilder();
    
            while (n > 0) {
                int remainder = n % 2;
                binary.insert(0, remainder);
                n = n / 2;
            }
    
            return Integer.parseInt(binary.toString());
        }
    }
```

[See on CodeWars.com](https://www.codewars.com/kata/59fca81a5712f9fa4700159a/train/java)