# CodeWars Java Solutions

---

## Twice as old

Your function takes two arguments:

current father's age (years)
current age of his son (years)
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old). The answer is always greater or equal to 0, no matter if it was in the past or it is in the future.




---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;


public class TwiceAsOldTest {
    @Test
    public void testSomething() {
        assertEquals(30, TwiceAsOld.TwiceAsOld(30,0));
        assertEquals(16, TwiceAsOld.TwiceAsOld(30,7));
        assertEquals(15, TwiceAsOld.TwiceAsOld(45,30));

    }
}
```

---

### Solution

```Java
public class TwiceAsOld{

  public static int TwiceAsOld(int dadYears, int sonYears){
    return Math.abs((sonYears * 2) - dadYears);
  }

}
```


[See on CodeWars.com](https://www.codewars.com/kata/5b853229cfde412a470000d0/train/java)