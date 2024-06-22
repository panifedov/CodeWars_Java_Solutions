# CodeWars Java Solutions

---

## altERnaTIng cAsE <=> ALTerNAtiNG CaSe

Define String.prototype.toAlternatingCase (or a similar function/method such as to_alternating_case/toAlternatingCase/ToAlternatingCase in your selected language; see the initial solution for details) such that each lowercase letter becomes uppercase and each uppercase letter becomes lowercase. For example:



```
    StringUtils.toAlternativeString("hello world") == "HELLO WORLD"
    StringUtils.toAlternativeString("HELLO WORLD") == "hello world"
    StringUtils.toAlternativeString("hello WORLD") == "HELLO world"
    StringUtils.toAlternativeString("HeLLo WoRLD") == "hEllO wOrld"
    StringUtils.toAlternativeString("12345") == "12345" // Non-alphabetical characters are unaffected
    StringUtils.toAlternativeString("1a2b3c4d5e") == "1A2B3C4D5E"
    StringUtils.toAlternativeString("StringUtils.toAlternatingCase") == "sTRINGuTILS.TOaLTERNATINGcASE"
```


As usual, your function/method should be pure, i.e. it should not mutate the original string.

---

### Given Code

```Java
    import org.junit.Test;

    import static org.junit.Assert.*;
    
    public class StringUtilsTest {
    
        @Test
        public void fixedTests() {
            assertEquals("HELLO WORLD", StringUtils.toAlternativeString("hello world"));
            assertEquals("hello world", StringUtils.toAlternativeString("HELLO WORLD"));
            assertEquals("HELLO world", StringUtils.toAlternativeString("hello WORLD"));
            assertEquals("hEllO wOrld", StringUtils.toAlternativeString("HeLLo WoRLD"));
            assertEquals("Hello World", StringUtils.toAlternativeString(StringUtils.toAlternativeString("Hello World")));
            assertEquals("12345", StringUtils.toAlternativeString("12345"));
            assertEquals("1A2B3C4D5E", StringUtils.toAlternativeString("1a2b3c4d5e"));
            assertEquals("sTRINGuTILS.TOaLTERNATINGcASE", StringUtils.toAlternativeString("StringUtils.toAlternatingCase"));
        }
    
        @Test
        public void kataTitleTests() {
            assertEquals("ALTerNAtiNG CaSe", StringUtils.toAlternativeString("altERnaTIng cAsE"));
            assertEquals("altERnaTIng cAsE", StringUtils.toAlternativeString("ALTerNAtiNG CaSe"));
            assertEquals("ALTerNAtiNG CaSe <=> altERnaTIng cAsE", StringUtils.toAlternativeString("altERnaTIng cAsE <=> ALTerNAtiNG CaSe"));
            assertEquals("altERnaTIng cAsE <=> ALTerNAtiNG CaSe", StringUtils.toAlternativeString("ALTerNAtiNG CaSe <=> altERnaTIng cAsE"));
        }
    }

```

---

### Solution

```Java
public class StringUtils {
  
  public static String toAlternativeString(String string) {
        StringBuilder result = new StringBuilder();
    
    for(char ch : string.toCharArray()){
      if(Character.isLowerCase(ch)){
        result.append(Character.toUpperCase(ch));
      }
      else if (Character.isUpperCase(ch)){
        result.append(Character.toLowerCase(ch));
      }
      else {
        result.append(ch);
      }
    };
    
    return result.toString();
  }
}
```

[See on CodeWars.com](https://www.codewars.com/kata/56efc695740d30f963000557/train/java)