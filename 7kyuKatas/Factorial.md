# CodeWars Java Solutions

---

## Factorial

Your task is to write function factorial.

https://en.wikipedia.org/wiki/Factorial
```

```

```

```



---

### Given Code

```Java
    import org.junit.jupiter.api.Test;
    import static org.junit.jupiter.api.Assertions.assertEquals;
    
    // TODO: Replace examples and use TDD by writing your own tests
    
    class SolutionTest {
        @Test
        void testSomething() {
            assertEquals(1L, Factorial.factorial(0));
            assertEquals(1L, Factorial.factorial(1));
            assertEquals(24L, Factorial.factorial(4));
            assertEquals(5040L, Factorial.factorial(7));
        }
    }

```

---

### Solution

``` Java
    public class Factorial {
    
        public static long factorial(int n) {
          if(n == 0){
            return 1L;
          }
          
          long result = 1L;
          
    
          for(int i = 1; i <= n; i++){
            result *= i;
          } 
    
            
          return result;
      }
    }
```


```Java
public class Factorial {

    public static long factorial(int n) {
        // your code here
        return n <= 1 ? 1 : n * factorial(n - 1);
    }
}
```
[See on CodeWars.com](https://www.codewars.com/kata/57a049e253ba33ac5e000212/train/java)