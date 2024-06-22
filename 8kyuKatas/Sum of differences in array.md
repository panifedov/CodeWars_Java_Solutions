# CodeWars Java Solutions

---

## Sum of differences in array


Your task is to sum the differences between consecutive pairs in the array in descending order.

```
[2, 1, 10]  -->  9
```

In descending order: [10, 2, 1]

Sum: (10 - 2) + (2 - 1) = 8 + 1 = 9

If the array is empty or the array has only one element the result should be 0 (Nothing in Haskell, None in Rust).



```

```


---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;

public class SolutionTest {

    @Test
    public void basicTests() {
        assertEquals(9, ZywOo.sumOfDifferences(new int[]{1, 2, 10}));
        assertEquals(2, ZywOo.sumOfDifferences(new int[]{-3, -2, -1}));
        assertEquals(0, ZywOo.sumOfDifferences(new int[]{1, 1, 1, 1, 1}));
        assertEquals(34, ZywOo.sumOfDifferences(new int[]{-17, 17}));
        assertEquals(0, ZywOo.sumOfDifferences(new int[0]));
        assertEquals(0, ZywOo.sumOfDifferences(new int[]{0}));
        assertEquals(0, ZywOo.sumOfDifferences(new int[]{-1}));
        assertEquals(0, ZywOo.sumOfDifferences(new int[]{1}));
    }
}
```

---

### Solution

```Java
public class ZywOo {

/*
  The idea is that such sum could be flatten. Example:
  [2, 1, 10]
  (10 - 2) + (2 - 1) = 8 + 1 = 9
  10 -2 + 2 -1 = 10 - 1
  So all elements except max and min will be used twice (one time with + and one tme ith -) so they will be erased.
*/
  public static int sumOfDifferences(int[] arr) {
    if (arr.length < 2) {
      return 0;
    }
  
    int min = arr[0];
    int max = arr[0];
    
    for (int i = 1; i < arr.length; i++) {
      if (arr[i] > max) {
        max = arr[i];
      }
      
      if (arr[i] < min) {
        min = arr[i];
      }
    }
    
    return max - min;
  }
}
```

```Java
import java.util.Arrays;

public class ZywOo {
  public static int sumOfDifferences(int[] arr) {
    if(arr == null || arr.length < 2){
      return 0;
    }
    
    Arrays.sort(arr);
    for (int i = 0; i < arr.length / 2; i++) {
      int temp = arr[i];
      arr[i] = arr[arr.length - 1 - i];
      arr[arr.length - 1 - i] = temp;
    }

    
    int result = 0;
    for(int i = 0; i < arr.length - 1; i++){
      result += (arr[i] - arr[i + 1]);
    }
    return result;
  }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/5b73fe9fb3d9776fbf00009e/train/java)