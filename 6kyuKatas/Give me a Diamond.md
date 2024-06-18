# CodeWars Java Solutions

---

## Give me a Diamond

Jamie is a programmer, and James' girlfriend. She likes diamonds, and wants a diamond string from James. Since James doesn't know how to make this happen, he needs your help.

Task
You need to return a string that looks like a diamond shape when printed on the screen, using asterisk (*) characters. Trailing spaces should be removed, and every line must be terminated with a newline character (\n).

Return null/nil/None/... if the input is an even number or negative, as it is not possible to print a diamond of even or negative size.

A size 3 diamond:
```
 *
***
 *
```
...which would appear as a string of " *\n***\n *\n"

A size 5 diamond:
```
 *
 ***
*****
 ***
  *
```
...that is:
```
"  *\n ***\n*****\n ***\n  *\n
```

---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import static org.junit.Assert.assertNull;

public class DiamondTest {
    @Test
    public void testDiamond3() {
        StringBuffer expected = new StringBuffer();
        expected.append(" *\n");
        expected.append("***\n");
        expected.append(" *\n");

        assertEquals(expected.toString(), Diamond.print(3));
    }

    @Test
    public void testDiamond5() {
        StringBuffer expected = new StringBuffer();
        expected.append("  *\n");
        expected.append(" ***\n");
        expected.append("*****\n");
        expected.append(" ***\n");
        expected.append("  *\n");

        assertEquals(expected.toString(), Diamond.print(5));
    }

    @Test
    public void testDiamond1() {
        StringBuffer expected = new StringBuffer();
        expected.append("*\n");
        assertEquals(expected.toString(), Diamond.print(1));
    }

    @Test
    public void testDiamond0() {
        assertEquals(null, Diamond.print(0));
    }

    @Test
    public void testDiamondMinus2() {
        assertEquals(null, Diamond.print(-2));
    }

    @Test
    public void testDiamond2() {
        assertEquals(null, Diamond.print(2));
    }
}

```

---

### Solution

``` Java
class Diamond {
  public static String print(int n) {
if (n < 0 || n % 2 == 0) {
            return null;
        }

        StringBuilder diamond = new StringBuilder();

        int middle = n / 2;
        for (int i = 0; i < n; i++) {
            int stars = i <= middle ? 2 * i + 1 : 2 * (n - i - 1) + 1;
            int spaces = (n - stars) / 2;
            
            diamond.append(repeat(" ", spaces))
                   .append(repeat("*", stars))
                   .append("\n");
        }

        return diamond.toString();
	}
  
      private static String repeat(String str, int times) {
        StringBuilder result = new StringBuilder();
        for (int i = 0; i < times; i++) {
            result.append(str);
        }
        return result.toString();
    }

}
```



[See on CodeWars.com](https://www.codewars.com/kata/5503013e34137eeeaa001648/train/java)