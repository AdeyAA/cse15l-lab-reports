 # cd
```
[user@sahara ~]$ cd
```
-The working directory when the line was run was the `home` directory.
We got this output because we gave no arguments so there is no directory to change to.
The output was not an error.

```
[user@sahara ~]$ cd lecture1
```
-The working directory when the line was run was the `lecture1` directory.
We got this output because we gave the argument of the `lecture1` directory, so we changed from the home directory to the `lecture1` directory.
The output was not an error.

```
[user@sahara ~/lecture1]$ cd README
bash: cd: README: Not a directory
```

-The working directory when the line was run was the `lecture1` directory.
We got this output because we have the argument of README which is not a directory but a file inside the `lecture1` directory, so this command would not work.
The output was an error stating that README is not a directory because README is a file.



```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
-The working directory when the line was run was the `lecture1` directory.
We got this output because the `ls` command lists all of the contents within the directory that you are currently in, so we got all the contents of the `lecture1` directory.
The output was not an error.

```
[user@sahara ~/lecture1]$ ls lecture1
ls: cannot access 'lecture1': No such file or directory
```
-The working directory when the line was run was the `lecture1` directory.
We got this output because here `lecture1` is the working directory but we also tried to use `lecture1` as an argument while we were already in the `lecture1` directory.
The output was an error that said `lecture1` was not able to be accessed because no such file or directory exists because there is no file or directory name `lecture1` inside the directory `lecture1`.

```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
```
-The working directory when the line was run was the `lecture1` directory.
We got this output because when you use the `ls` command and then add a file that is in the directory next to the command the output that you get is all the contents that are within that file.
The output was not an error.





```
[user@sahara ~/lecture1]$ cat
```
-The working directory when the line was run was the `lecture1` directory.
We got this output because the `cat` command expects that an argument will be added after it and since we did not add an argument after the `cat` command nothing happened when the command was executed because there was nothing for the command to read.
The output was not an error.

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```

-The working directory when the line was run was the `home` directory. We got this output because here we are in the `home` directory and the `cat` command was given an argument of the `lecture1` directory when it should have been given the argument of a file. The output was an error because the cat command is supposed to be given an argument of a file but we gave it the argument of a directory so the message is telling us that we provided a directory but we should have given it a file.


```
[user@sahara ~/lecture1]$ cat README
To use this program:

javac Hello.java
java Hello messages/en-us.txt
```         

-The working directory when the line was run was the `lecture1` directory. 
We got this output because here we are asking the command `cat' while in the `lecture1` directory read the file titled README and the contents of that file are printed.
The output was not an error.

