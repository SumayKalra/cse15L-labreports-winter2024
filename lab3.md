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
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/45e8d71b-7682-4868-8465-137cd278974f)

PreFix:
'''
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
'''

PostFix:
'''
static void reverseInPlace(int[] arr) {
  for (int i = 0; i < arr.length / 2; i++) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
'''

# Part 2: Command Research
Command Chosen:
'''find'''

Option 1:
'''-type''' 
Example 1: 
'''find ./technical -type d'''
Output 1: 
''' 
./technical/
./technical/911report
./technical/biomed
./technical/government
./technical/plos
'''

Example 2:
'''find ./technical -type f -executable'''
Output 2:
'''         '''

Option 2:
'''-name'''

Example 1:
'''find ./technical -name "Progress_report.txt" '''
Output 1:
''' ./technical/government/About_LSC/Progress_report.txt'''

Example 2:
'''find ./technical -name "Doesnotexit.txt" '''
Output 2:
'''       '''

Option 3:
'''-mtime'''

Example 1:
'''find ./technical -mtime -7'''
Output 1:
'''          '''

Example 2:
'''find ./technical -mtime +1000'''
Output 2: 
'''        '''

Option 4:
'''-exec'''

Example 1:
'''find ./technical '''






