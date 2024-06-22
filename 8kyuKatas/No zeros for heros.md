# CodeWars Java Solutions

---

## No zeros for heros

Numbers ending with zeros are boring.

They might be fun in your world, but not here.

Get rid of them. Only the ending ones.

```
    1450 -> 145
    960000 -> 96
    1050 -> 105
    -1050 -> -105
```

Zero alone is fine, don't worry about it. Poor guy anyway

---

### Given Code

```Java
    import static org.junit.Assert.*;
    import org.junit.Test;

    public class NoBoringTest {

        private static void testing(int actual, int expected) {
            assertEquals(expected, actual);
        }
        @Test
        public void test1() {
            System.out.println("Fixed Tests: noBoringZeros");
            testing(NoBoring.noBoringZeros(1450), 145);
            testing(NoBoring.noBoringZeros(960000), 96);
            testing(NoBoring.noBoringZeros(1050), 105);
            testing(NoBoring.noBoringZeros(-1050), -105);
        }
    }

```

---

### Solution

```Java
public class NoBoring {
    public static int noBoringZeros(int n) {
      String numberStr = Integer.toString(n);
      numberStr = numberStr.replaceAll("0*$", "");

      if(numberStr.isEmpty()){
        return 0;
      }  
      
      return Integer.parseInt(numberStr);
    }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/570a6a46455d08ff8d001002/train/java)