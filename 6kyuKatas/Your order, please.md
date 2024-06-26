# CodeWars Java Solutions

---

## Your order, please
Your task is to sort a given string. Each word in the string will contain a single number. This number is the position the word should have in the result.

Note: Numbers can be from 1 to 9. So 1 will be the first word (not 0).

If the input string is empty, return an empty string. The words in the input String will only contain valid consecutive numbers.

```
"is2 Thi1s T4est 3a"  -->  "Thi1s is2 3a T4est"
"4of Fo1r pe6ople g3ood th5e the2"  -->  "Fo1r the2 g3ood 4of th5e pe6ople"
""  -->  ""
```




---

### Given Code

```Java
import static org.junit.Assert.*;
import org.junit.Test;
import static org.hamcrest.CoreMatchers.*;

public class OrderTest {
    @Test
    public void test1() {
        assertThat(Order.order("is2 Thi1s T4est 3a"), equalTo("Thi1s is2 3a T4est"));
    }

    @Test
    public void test2() {
        assertThat(Order.order("4of Fo1r pe6ople g3ood th5e the2"), equalTo("Fo1r the2 g3ood 4of th5e pe6ople"));
    }

    @Test
    public void test3() {
        assertThat("Empty input should return empty string", Order.order(""), equalTo(""));
    }
}
```

---

### Solution


```Java
import java.util.Arrays;
import java.util.Comparator;

public class Order {
    public static String order(String words) {
        if (words == null || words.isEmpty()) {
            return "";
        }

        String[] splitWords = words.split(" ");

        Arrays.sort(splitWords, new Comparator<String>() {
            public int compare(String word1, String word2) {
                return getNumber(word1) - getNumber(word2);
            }

            private int getNumber(String word) {
                for (char c : word.toCharArray()) {
                    if (Character.isDigit(c)) {
                        return Character.getNumericValue(c);
                    }
                }
                return -1;
            }
        });

        return String.join(" ", splitWords);
    }
}
```



[See on CodeWars.com](https://www.codewars.com/kata/55c45be3b2079eccff00010f/train/java)