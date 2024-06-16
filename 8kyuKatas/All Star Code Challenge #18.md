# CodeWars Java Solutions

---

## All Star Code Challenge #18

Create a function that accepts a string and a single character, and returns an integer of the count of occurrences the 2nd argument is found in the first one.

If no occurrences can be found, a count of 0 should be returned.

```
    ("Hello", "o")  ==>  1
    ("Hello", "l")  ==>  2
    ("", "z")       ==>  0
```

```
    str_count("Hello", 'o'); // returns 1
    str_count("Hello", 'l'); // returns 2
    str_count("", 'z'); // returns 0
```

Notes
The first argument can be an empty string
In languages with no distinct character data type, the second argument will be a string of length 1

---

### Given Code

```Java
    import org.junit.Test;
    import static org.junit.Assert.assertEquals;
    import org.junit.runners.JUnit4;

    public class basicTests {
        @Test
        public void testSomething() {
            assertEquals(1, CodeWars.strCount("Hello", 'o'));
            assertEquals(2, CodeWars.strCount("Hello", 'l'));
            assertEquals(0, CodeWars.strCount("",'z'));
        }
    }

```

---

### Solution

``` Java
public class CodeWars {
  public static int strCount(String str, char letter) {
    int count = 0;
    for(char ch : str.toCharArray()){
      if(ch == letter){
        count++;
      }
    }
    return count;
  }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/5865918c6b569962950002a1/train/java)