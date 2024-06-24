# CodeWars Java Solutions

---

## Row Weights

Scenario
Several people are standing in a row divided into two teams.
The first person goes into team 1, the second goes into team 2, the third goes into team 1, and so on.

Task
Given an array of positive integers (the weights of the people), return a new array/tuple of two integers, where the first one is the total weight of team 1, and the second one is the total weight of team 2.

Notes
Array size is at least 1.
All numbers will be positive.
Input >> Output Examples
```
rowWeights([13, 27, 49])  ==>  return (62, 27)

```
Explanation:
The first element 62 is the total weight of team 1, and the second element 27 is the total weight of team 2.

```
rowWeights([50, 60, 70, 80])  ==>  return (120, 140)

```
Explanation:
The first element 120 is the total weight of team 1, and the second element 140 is the total weight of team 2.

```
rowWeights([80])  ==>  return (80, 0)


```
Explanation:
The first element 80 is the total weight of team 1, and the second element 0 is the total weight of team 2.

Playing with Numbers Series
Playing With Lists/Arrays Series
For More Enjoyable Katas
ALL translations are welcomed
Enjoy Learning !!
Zizou

---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertArrayEquals;
import org.junit.runners.JUnit4;

public class Row_Weights
{
    @Test
    public void Basic_Tests()
    {
        assertArrayEquals(new int[]{80,0}, Solution.rowWeights(new int[]{80}));
        assertArrayEquals(new int[]{100,50}, Solution.rowWeights(new int[]{100,50}));
        assertArrayEquals(new int[]{120,140}, Solution.rowWeights(new int[]{50,60,70,80}));
    }
    @Test
    public void Odd_Vector_Length()
    {
        assertArrayEquals(new int[]{62,27}, Solution.rowWeights(new int[]{13,27,49}));
        assertArrayEquals(new int[]{236,92}, Solution.rowWeights(new int[]{70,58,75,34,91}));
        assertArrayEquals(new int[]{211,164}, Solution.rowWeights(new int[]{29,83,67,53,19,28,96}));
    }
    @Test
    public void Even_Vector_Length()
    {
        assertArrayEquals(new int[]{100,50}, Solution.rowWeights(new int[]{100,50}));
        assertArrayEquals(new int[]{150,151}, Solution.rowWeights(new int[]{100,51,50,100}));
        assertArrayEquals(new int[]{207,235}, Solution.rowWeights(new int[]{39,84,74,18,59,72,35,61}));
    }
}
```

---

### Solution


```Java
public class Solution
{
    public static int[] rowWeights (final int[] weights)
    {
        int[] result = new int[2];
        int countOne = 0;
        int countTwo = 0;

        for(int i = 0; i < weights.length; i++) {
            if(i % 2 == 0) {
                countOne += weights[i];
            } else {
                countTwo += weights[i];
            }
        }

        result[0] = countOne;
        result[1] = countTwo;

        return result; // Do your magic!
    }
}
```



[See on CodeWars.com](https://www.codewars.com/kata/5abd66a5ccfd1130b30000a9/train/java)