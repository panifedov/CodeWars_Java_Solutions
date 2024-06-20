# CodeWars Java Solutions

---

## Lario and Muigi Pipe Problem

Issue
Looks like some hoodlum plumber and his brother has been running around and damaging your stages again.

The pipes connecting your level's stages together need to be fixed before you receive any more complaints.

The pipes are correct when each pipe after the first is 1 more than the previous one.

Task
Given a list of unique numbers sorted in ascending order, return a new list so that the values increment by 1 for each index from the minimum value up to the maximum value (both included).

```dtd
Input:  1,3,5,6,7,8 Output: 1,2,3,4,5,6,7,8
```

---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertArrayEquals;

public class PipesExampleTests {
    @Test
    public void tests() {
        assertArrayEquals(new int[] {1,2,3,4,5,6,7,8,9}, Kata.pipeFix(new int[] {1,2,3,5,6,8,9}));
        assertArrayEquals(new int[] {1,2,3,4,5,6,7,8,9,10,11,12}, Kata.pipeFix(new int[] {1,2,3,12}));
        assertArrayEquals(new int[] {6,7,8,9}, Kata.pipeFix(new int[] {6,9}));
        assertArrayEquals(new int[] {-1,0,1,2,3,4}, Kata.pipeFix(new int[] {-1,4}));
        assertArrayEquals(new int[] {1,2,3}, Kata.pipeFix(new int[] {1,2,3}));
    }
}

```

---

### Solution

``` Java
public class Kata {
  public static int[] pipeFix(int[] numbers) {
        int min = numbers[0];
        int max = numbers[numbers.length - 1];
        
        
        int[] result = new int[max - min + 1];
        
        
        for (int i = 0; i < result.length; i++) {
            result[i] = min + i;
        }
        
        return result;
  }
}
```



[See on CodeWars.com](https://www.codewars.com/kata/56b29582461215098d00000f/train/java)