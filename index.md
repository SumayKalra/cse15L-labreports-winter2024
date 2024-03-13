**Debugging Scenario**

1. Classmate: Why is the expected value for the solution true when it is supposed to be false? This is not a palindrome so let's find this out together!

   ```
   public boolean isPalindrome(int x) {
        if (x < 0 || (x % 10 == 0 && x != 0)) {
            return false;
        }
        int reversed = 0;
        while (x > reversed) {
            reversed = reversed * 10 + x % 10;
            x /= 10;
        }
        return !(x == reversed || x == reversed / 10);
    }
```

```
@Test
public void testPalindromeNum() {
        PalindromeNumber solution = new PalindromeNumber();
        int target = 19234;
        int[] expected = False;
        int[] actual = solution.isPalindrome(target);
        assertArrayEquals(expected, actual);
}
```
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/f00d7233-79cf-48b1-89d9-43b07175ed6c)

2. TA: You should add a print statement within your code to see why it is not working and why you get the opposite answer each time

3. Students Utilization of Advice
```
  public boolean isPalindrome(int x) {
        if (x < 0 || (x % 10 == 0 && x != 0)) {
            return false;
        }
        int reversed = 0;
        while (x > reversed) {
            reversed = reversed * 10 + x % 10;
            x /= 10;
            System.out.println(reversed);
        }
        return !(x == reversed || x == reversed / 10);
    }
```
![unnamed](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/b9680b77-df2b-44c3-b5fb-ad73c82beea1)
The bug is located on line 17 as we recognize through the print statement that the code realizes it is false, but for some reason just keeps pushing the fact that its true or vice versa, and that is because in the exclamation mark in the return statement switches the boolean value to the incorrect one, thus, by simply removing it we ensure that the code has now been fixed.

```
public class lab5 {
    int x;
    public lab5(int x){
    this.x = x;
    }
    
    public boolean isPalindrome() {
        if (x < 0 || (x % 10 == 0 && x != 0)) {
            return false;
        }
        int reversed = 0;
        while (x > reversed) {
            reversed = reversed * 10 + x % 10;
            x /= 10;
            System.out.println(reversed);
        }
        return !(x == reversed || x == reversed / 10);
    }
}
```
Directories:
```
lab5/
|-  starter/
    |-  PublicTester.class
  	|-  PublicTester.java
  	|-  lab5.class
  	|-  lab5.java
  	|-  test.sh
|-  libs/
  	|-  hamcrest-2.2.jar
  	|-  junit-4.13.2.jar
```

PublicTester.java:
```
package lab5.starter;

import org.junit.Test;
import static org.junit.Assert.assertArrayEquals;

public class PublicTester {

    @Test
    public void testPalindromeNum() {
        int target = 19234;
        boolean expected = false; 
        lab5 lab = new lab5(); 
        boolean actual = lab.isPalindrome(target);
        assertEquals(expected, actual); 
    }
}
```

lab5.java:
```
public class lab5 {
    int x;
    public lab5(int x){
    this.x = x;
    }
    
    public boolean isPalindrome() {
        if (x < 0 || (x % 10 == 0 && x != 0)) {
            return false;
        }
        int reversed = 0;
        while (x > reversed) {
            reversed = reversed * 10 + x % 10;
            x /= 10;
        }
        return !(x == reversed || x == reversed / 10);
    }
}
```
test.sh: <br/>
`javac -cp ../libs/junit-4.13.2.jar:../libs/hamcrest-2.2.jar:. PublicTester.java` 
`java -cp ../libs/junit-4.13.2.jar:../libs/hamcrest-2.2.jar:. org.junit.runner.JUnitCore PublicTester`

Command Lines: `bash test.sh `
Fixing bug: Remove ! from the return statement that switched the boolean from true to false or false to true

# Reflection
I think the coolest thing that I learned in the second half of the quarter would be the vim commands to navigate through vim, as in my lab at the med school I would tediously go through bash and vim code to edit certain things with raspberry pis, as I never heard of these short cuts. Now my job has become alot easier so thank you cse 15L!
