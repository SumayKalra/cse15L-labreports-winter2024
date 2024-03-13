# LAB 4 VIM

STEP 4:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/59a777af-d7c3-4a45-a9f7-8b156c971cf9)
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/d96d8e4e-0d40-4b05-82e1-ad85af5ef4de)


Key: ```ssh<space>sukalra@ieng6.ucsd.edu<return>```

This command allows us to access the UCSD computer to do the lab on this instead as we need to
STEP 5:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/4c7a67ca-9cad-460f-8501-90e56502f0df)

Key: ```git<space>clone<space>git@github.com:ucsd-cse15l-s23/lab7.git>return>```

Here we clone the git lab7 into our remote server to use for the remainder of the lab

STEP 6:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/984d9d22-0daf-4384-a935-ad457d474fc1)
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/83706e1d-53f8-458b-ab60-f81bc9251d40)

Key: ```cd<space>lab7<return>``` and ```bash<space>test.sh<return>```

We go to the lab 7 directory and we run the testing bash script to see what tests are failing and what we need to fix

STEP 7:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/882949fe-57d9-4582-8910-6451c4fffc93)

Key:```vim<space>ListExampls.java<return>``` and  ```43jexi2<esc>:wq```

Using vim we open up the java script to edit, and we go down 43 lines using 43j, then e to go to the end of the next word, then x to delete one element, and then i to insert something, in which we insert 2, we hit escape to leave that area and then :wq to get out of vim and back to the command line

STEP 8:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/dda3d98e-2a14-4578-b877-da999ee20122)
Key:  ```bash<space>test.sh```

This is to retest our new and imporved java script

STEP 9:
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/d3618db8-c98a-4393-986c-cff7dc668d46)
![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/51f40303-424d-48cf-bafa-095d0493b2c3)

Keys: ```git<space>add<space>.<return>```  and ```git<space>commit<space>-m<space>"fixed<space>the<space>java<space>script<space>so<space>all<space>tests<space>pass"<return>``` and ```git<space>push<return>```

Now that we have fixed the script we must update it on github, so we use git add to save those changes and git commit - m to send a message on what those changes were and what they did
