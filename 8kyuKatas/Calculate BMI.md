# CodeWars Java Solutions

---

## Calculate BMI

Write function bmi that calculates body mass index (bmi = weight / height2).

if bmi <= 18.5 return "Underweight"

if bmi <= 25.0 return "Normal"

if bmi <= 30.0 return "Overweight"

if bmi > 30 return "Obese"


---

### Given Code

```Java
import org.junit.Test;
import static org.junit.Assert.assertEquals;
import org.junit.runners.JUnit4;

public class SolutionTest {
    @Test
    public void testBMI() {
        assertEquals("Normal", Calculate.bmi(80, 1.80));
    }
}

```

---

### Solution

```Java
public class Calculate {
  public static String bmi(double weight, double height) {
    double bmi = weight/(height*height);
    
    
    if(bmi < 18.5){
      return "Underweight";
    }
    if(bmi < 25.0){
      return "Normal";
    }
    if(bmi < 30.0){
      return "Overweight";
    }
    else{
      return "Obese";
    }
    
  }
}
```

### Solution 2

```Java
public class Calculate {
public static String bmi(double weight, double height) {
double bmi =weight/(height*height);
return bmi <= 18.5 ? "Underweight": bmi <=25.0 ? "Normal" : bmi<=30.0 ? "Overweight" : "Obese";
}
}
```

[See on CodeWars.com](https://www.codewars.com/kata/57a429e253ba3381850000fb/train/java)