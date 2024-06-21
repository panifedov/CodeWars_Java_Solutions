# CodeWars Java Solutions

---

## Form The Minimum

Task
Given a list of digits, return the smallest number that could be formed from these digits, using the digits only once (ignore duplicates).

Notes:
Only positive integers will be passed to the function (> 0 ), no negatives or zeros.
Input >> Output Examples

```
minValue ({1, 3, 1})  ==> return (13)
```
Explanation:
(13) is the minimum number could be formed from {1, 3, 1} , Without duplications

```
minValue({5, 7, 5, 9, 7})  ==> return (579)
```

Explanation:
(579) is the minimum number could be formed from {5, 7, 5, 9, 7} , Without duplications

```
minValue({1, 9, 3, 1, 7, 4, 6, 6, 7}) return  ==> (134679)
```

Explanation:
(134679) is the minimum number could be formed from {1, 9, 3, 1, 7, 4, 6, 6, 7} , Without duplications
---

Playing with Numbers Series
Playing With Lists/Arrays Series
Bizarre Sorting-katas
For More Enjoyable Katas
ALL translations are welcomed
Enjoy Learning !!
Zizou

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;



public class SolutionTest {
    @Test
    public void testSomething() {
        assertEquals(13, Minimum.minValue(new int[] {1,3,1}));
        assertEquals(457, Minimum.minValue(new int[] {4, 7, 5, 7}));
        assertEquals(148, Minimum.minValue(new int[] {4, 8, 1, 4}));
        assertEquals(579, Minimum.minValue(new int[] {5, 7, 9, 5, 7}));
        assertEquals(678, Minimum.minValue(new int[] {6, 7, 8, 7, 6, 6}));
    }
}

```

---

### Solution

``` Java

```

[See on CodeWars.com](https://www.codewars.com/kata/5ac6932b2f317b96980000ca/train/java)