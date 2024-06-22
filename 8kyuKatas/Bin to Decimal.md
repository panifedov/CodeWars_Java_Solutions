# CodeWars Java Solutions

---

## Bin to Decimal

Complete the function which converts a binary number (given as a string) to a decimal number.

```

```

```

```


---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;

public class ConverterTest {

    @Test
    public void testHoopCount() {
        assertEquals(1, Converter.binToDecimal("1"));
        assertEquals(0, Converter.binToDecimal("0"));
        assertEquals(73, Converter.binToDecimal("1001001"));
    }
}

```

---

### Solution

```Java
public class Converter{
  public static int binToDecimal(String inp){
    return Integer.parseInt(inp, 2);
  }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/57a5c31ce298a7e6b7000334/train/java)