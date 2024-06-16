# CodeWars Java Solutions

---

## The Wide-Mouthed frog!

The wide-mouth frog is particularly interested in the eating habits of other creatures.

He just can't stop asking the creatures he encounters what they like to eat. But, then he meets the alligator who just LOVES to eat wide-mouthed frogs!

When he meets the alligator, it then makes a tiny mouth.

Your goal in this kata is to create complete the mouth_size method this method takes one argument animal which corresponds to the animal encountered by the frog. If this one is an alligator (case-insensitive) return small otherwise return wide.
```
    
```



---

### Given Code

```Java
    import org.junit.Test;
    import static org.junit.Assert.assertEquals;
    import org.junit.runners.JUnit4;
    
    public class WideMouthedFrogTest {
    
        @Test
        public void fixedTests() {
            assertEquals("wide", WideMouthedFrog.mouthSize("toucan"));
            assertEquals("wide",WideMouthedFrog.mouthSize("ant bear"));
            assertEquals("small", WideMouthedFrog.mouthSize("alligator"));
        }
    }

```

---

### Solution

```Java
    public class WideMouthedFrog{
    public static String mouthSize(String animal){
        return animal.equalsIgnoreCase("alligator") ? "small" : "wide";
    }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/57ec8bd8f670e9a47a000f89/train/java)