# Part 1: Bugs

Fail:
```
@Test 
public void testReverseInPlace() {
  int[] input1 = { 3,4,5 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 5,4,3 }, input1);
}
```

No Fail:
```
@Test
public void testReverseInPlace2() {
  int[] input1 = { 3 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 3 }, input1);
}
```
running tests:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/c2ad2f55-3734-4f93-a5a6-22fbf3228cb9)

PreFix:
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

PostFix:
```
static void reverseInPlace(int[] arr) {
  for (int i = 0; i < arr.length / 2; i++) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```
The prior code would set the elements in the middle of the array, to the new ones instead of the original ones as it should be doing. What this new fix does is it stops that swapping as we approach the middle so our solution has become ideal with no issues!


# Part 2: Command Research
Command Chosen:
```find```

**Warning: If an Output looks like its blank that means there is no output**

Option 1:
```type``` 

Example 1: 
```find ./technical -type d```
Output 1: 
``` 
./technical/
./technical/911report
./technical/biomed
./technical/government
./technical/plos
```
This is good for showing all the directories in a folder.

Example 2:
```find ./technical -type f -executable```

Output 2:
```         ```

This is good to see if there is any executable code in a folder.

_________________________________________________________________________________

Option 2:
```name```

Example 1:
```find ./technical -name "Progress_report.txt" ```

Output 1:
``` ./technical/government/About_LSC/Progress_report.txt```

This is good for finding the path of a specific text file.

Example 2:
```find ./technical -name "Doesnotexit.txt" ```

Output 2:
```       ```

In this case what happens is the file does not exist which is good to know if your looking for a file.

_________________________________________________________________________________


Option 3:
```-mtime```

Example 1:
```find ./technical -mtime -7```

Output 1:
```          ```

This line asks the machine if any files have been edited in the past 7 days which is good to know when coding with alot of people.

Example 2:
```find ./technical -mtime +1000```

Output 2: 
```        ```

Similarly, this line checks if any file has been edited in the last 1000 days which is good information to know.

_________________________________________________________________________________


Option 4:
```-size```

Example 1:
```find ./technical -type f - size +1000M```

Output 1:
```          ```

This outputs all the files over 1000 mbs which is good to see for storage reasons.

Example 2:
```find ./technical -type f - size -1k```

Output 2:
```          ```


This outputs all the files below 1 kb which is also good for storage reasons.

General comment: Alot of these commands lead to no output in ./technical due to the limited environment ./technical provides

Source: Chat gpt prompt and output in the image
I got the general info of what you can do with find and applied it to the ./technical GitHub.
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/a3d440d5-bbdd-4a97-9b82-431107e01518)
