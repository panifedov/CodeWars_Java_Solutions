# CodeWars Java Solutions

---

## Grasshopper - Messi Goals

Messi's Goal Total
Use variables to find the sum of the goals Messi scored in 3 competitions

Information
Messi goal scoring statistics:

Competition	Goals
La Liga	43
Champions League	10
Copa del Rey	5
Task
Create these three variables and store the appropriate values using the table above:
laLigaGoals
championsLeagueGoals
copaDelReyGoals
Create a fourth variable named totalGoals that stores the sum of all of Messi's goals for this year.
---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;

public class GoalsTest {
    @Test
    public void BasicTests() {
        assertEquals(58, Goals.totalGoals);
    }
}
```

---

### Solution

```Java
public class Goals {
    public static int laLigaGoals = 43;
    public static int championsLeagueGoals = 10;
    public static int copaDelReyGoals = 5;
    public static int totalGoals = laLigaGoals + championsLeagueGoals + copaDelReyGoals;

    public static void main(String[] args) {
        System.out.println("Total goals scored by Messi: " + totalGoals);
    }
}
```

[See on CodeWars.com](  https://www.codewars.com/kata/55ca77fa094a2af31f00002a/train/java)