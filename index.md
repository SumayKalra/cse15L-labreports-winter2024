<h3 id="custom-id">LAB 1 cd/cat/ls question</h3>



<h3 id="custom-id">CD Nothing</h3>

```
[user@sahara ~] $ cd
[user@sahara ~] $
```

If you don't cd anything in the terminal it will do nothing as cd'ing is used to go into a directory and gain access to other things such as more directories or files. Not an error but nothing happened.


<h3 id="custom-id">CD Directory</h3>
```
[user@sahara ~] $ cd lecture1
[user@sahara ~/lecture1] $
```

If you cd a directory in the terminal you will gain access to the contents of that directory which could include more directories and files. Not an error

<h3 id="custom-id">CD File</h3>
```
[user@sahara ~/lecture1] $ cd Hello.java
bash cd: Hello.java: Not a directory
```

If you cd a file you will get a message letting you now you cant cd a file as it is meant for directories and a file only hold code or txt or images etc and does not have more directories or files within them to be accessed you can think of it like a folder with pieces of paper, you can access a folder to get to more folders and pieces of paper, but you cant access pieces of paper. This is an error


<h3 id="custom-id">LS Nothing</h3>
```
[user@sahara ~] $ ls
lecture1
```

If you ls nothing you will just see the highlighted folder shown which is the file/folder you are out of, and the files outside of it For example if you are in no folders then it will show all the outside folders from your user cd, thus since here we are out of all folders we show the only folder on the outside which is lecture. this is not an error


<h3 id="custom-id">LS Directory</h3>
```
[user@sahara ~] $ ls lecture1
Hello.class Hello.java messages README
```

If you ls a directory you will see all the other folders in the directory plus any other files, which is useful so you can either cd into another directory or see all the files in a folder displayed! This is not an error. If directory name is not found this would be an error.

<h3 id="custom-id">LS File</h3>
```
[user@sahara ~/lecture1] $ ls Hello.class
Hello.class 
```

If you ls a file you just see that file name displayed as there are no other files or directories within that file, thus this function is kinda useless as you only get the file name as an output. This is an error. If file name is not found there would be an error.

<h3 id="custom-id">CAT Nothing</h3>
```
[user@sahara ~/] $ cat 
^C
```

If you cat nothing the computer seems to run something and can not stop it, thus you are forced to hit control C to stop running the machine so you can execute another line of code in the terminal. This is not a error.


<h3 id="custom-id">CAT Directory</h3>
```
[user@sahara ~/] $ cat lecture1
cat: lecture1: is a directory
```

If you cat a directory you will get an error as a cat cannot print whatever is in that directory as it contains more files and possibly directories, however, it will tell you that it is a directory thus you can learn from your mistake and continue . This is an error


<h3 id="custom-id">CAT File</h3>
```
[user@sahara ~/] $ cat lHello.java 
Hello World
```

If you cat a file you will get returned the contents of that file, even if you are not in a further away directory on the directory tree, thus this feature is useful for time efficiency! This is not an error but if the file name did not exist it would be an error. It is important to realize these commands are all done through the home directory as that is the use of cat.


| | image      | explanation | 
| :--- | :---        |    :----:   |  
| cd |![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/f72b493e-7768-4c7f-be8d-2772abba95af) | Cd nothing: you arent entering into anything directory; Cd directory: you have cd'd into the directory lecture ; cd file: does not work as cd is for directories| 
| ls |![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/d4349f31-af6e-456e-baad-b676d36ab408) | ls nothing: shows all directories under the main branch (lecture1); ls lecture1: shoes all directories and files within lecture1 directory; ls file: does not work as there is nothing in the file | 
| cat |![image](https://github.com/SumayKalra/cse15L-labreports-winter2024/assets/67125138/b63aad6c-7f3a-4dbd-b1b7-2f20b8353007)| cat nothing: does nothing and need to control C to get out of the terminal makes it get stuck pretty much; cat directory: you can not cat a directory and there is nothing to run; cat file: simply just runs the file | 
