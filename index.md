# LAB 4 VIM

STEP 4:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/cd18b4f8-d041-41d1-afeb-1c9abdbb9958)

Key: ```ssh sukalra@ieng6.ucsd.edu```

This command allows us to access the UCSD computer specifically port 201 because 203 does not have java and that caused me some issues

STEP 5:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/4c7a67ca-9cad-460f-8501-90e56502f0df)

Key: ```git clone https://github.com/ucsd-cse15l-s23/lab7```

Here we clone the git lab7 into our remote server to use for the remainder of the lab

STEP 6:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/984d9d22-0daf-4384-a935-ad457d474fc1)
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/83706e1d-53f8-458b-ab60-f81bc9251d40)

Key: ```cd lab7``` and ```bash test.sh```

We go to the lab 7 directory and we run the testing bash script to see what tests are failing and what we need to fix

STEP 7:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/882949fe-57d9-4582-8910-6451c4fffc93)

Key:```vim ListExampls.java<return>``` and  ```43jexi2<esc>:wq```

Using vim we open up the java script to edit, and we go down 43 lines using 43j, then e to go to the end of the next word, then x to delete one element, and then i to insert something, in which we insert 2, we hit escape to leave that area and then :wq to get out of vim and back to the command line

STEP 8:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/dda3d98e-2a14-4578-b877-da999ee20122)
Key:  ```bash test.sh```

This is to retest our new and imporved java script

STEP 9:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/d3618db8-c98a-4393-986c-cff7dc668d46)
Keys: ```git add .<return>```  and ```git commit -m "fixed the java script so all tests pass"<return>```

Now that we have fixed the script we must update it on github, so we use git add to save those changes and git commit - m to send a message on what those changes were and what they did
