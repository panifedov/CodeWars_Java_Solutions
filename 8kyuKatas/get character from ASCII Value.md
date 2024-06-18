# CodeWars Java Solutions

---

## get character from ASCII Value

Write a function which takes a number and returns the corresponding ASCII char for that value.

```
65 --> 'A'
97 --> 'a'
48 --> '0
```
For ASCII table, you can refer to http://www.asciitable.com/



---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;

public class SolutionTest {
    @Test
    public void testChar() {
        assertEquals('7', Ascii.getChar(55));
        assertEquals('8', Ascii.getChar(56));
        assertEquals('9', Ascii.getChar(57));
        assertEquals(':', Ascii.getChar(58));
        assertEquals(';', Ascii.getChar(59));
        assertEquals('<', Ascii.getChar(60));
        assertEquals('=', Ascii.getChar(61));
        assertEquals('>', Ascii.getChar(62));
        assertEquals('?', Ascii.getChar(63));
        assertEquals('@', Ascii.getChar(64));
        assertEquals('A', Ascii.getChar(65));
        assertEquals("getChar should return a `char`", 0, Character.compare('!', Ascii.getChar(33)));
    }
}
```

---

### Solution

``` Java
public class Ascii {
  public static char getChar(int c) {
    return (char) c;
  }
}
```
``` Java
ublic class Ascii {
public static char getChar(int c) {
char[] ascii = {'#', '#', '#', '#', '#', '#', '#', '#', '#', '#',
'#', '#', '#', '#', '#', '#', '#', '#', '#', '#',
'#', '#', '#', '#', '#', '#', '#', '#', '#', '#',
'#', '#', ' ', '!', '"', '#', '$', '%', '&', '\'',
'(', ')', '*', '+', ',', '-', '.', '/', '0', '1',
'2', '3', '4', '5', '6', '7', '8', '9', ':', ';',
'<', '=', '>', '?', '@', 'A', 'B', 'C', 'D', 'E',
'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'M', 'O',
'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y',
'Z', '[', '\\', ']', '^', '_', '`', 'a', 'b', 'c',
'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w',
'x', 'y', 'z', '{', '|', '}', '~', '#', '#', '#',};
return ascii[c];                 
}

}
```
[See on CodeWars.com](https://www.codewars.com/kata/55ad04714f0b468e8200001c/train/java)