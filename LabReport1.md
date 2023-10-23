# Lab 1: Remote Access and FileSystem

In this lab report, I will walk you through the fundamental filesystem commands we learned today, specifically cd, ls, and cat. We'll explore how these commands work with various arguments and scenarios.

### cd Command
1: Using cd with No Arguments
![Image](1.png | width=100)
Working Directory: /home
Output: No output
Explanation: Running cd without any arguments takes you to your home directory. 

2: Using cd with a Directory Path
```
$ cd lecture1
$
```
Working Directory: /home
Output: No output.
Explanation: When you use cd with a directory path, you change your working directory to the specified directory. In this case, we navigated to /path/to/directory.

Example 3: Using cd with a Nonexistent Directory Path
shell
Copy code
$ cd /nonexistent/directory
Working Directory: The current working directory.
Output: An error message - "No such file or directory."
Explanation: If you try to cd into a directory that doesn't exist, you'll receive an error because the specified directory is not found in the filesystem.

ls Command
Example 1: Using ls with No Arguments
shell
Copy code
$ ls
Working Directory: The current working directory.
Output: List of files and directories in the current working directory.
Explanation: Running ls without arguments will display the contents of the current working directory. This is a quick way to see what's in the directory you're in.

Example 2: Using ls with a Directory Path
shell
Copy code
$ ls /path/to/directory
Working Directory: The current working directory.
Output: List of files and directories in the specified directory.
Explanation: When you use ls with a directory path, it shows the contents of the specified directory without changing your working directory.

Example 3: Using ls with a Nonexistent Directory Path
shell
Copy code
$ ls /nonexistent/directory
Working Directory: The current working directory.
Output: An error message - "No such file or directory."
Explanation: If you attempt to ls a directory that doesn't exist, you'll receive an error because the specified directory is not found in the filesystem.

cat Command
Example 1: Using cat with No Arguments
shell
Copy code
$ cat
Working Directory: The current working directory.
Output: An error message - "No such file or directory."
Explanation: Running cat without any arguments is incorrect as it expects a file to be specified. Hence, it's an error.

Example 2: Using cat with a File Path
shell
Copy code
$ cat file.txt
Working Directory: The current working directory.
Output: The content of the "file.txt" file.
Explanation: When you use cat with a file path, it displays the content of the specified file. In this case, it shows the content of "file.txt."

Example 3: Using cat with a Nonexistent File
shell
Copy code
$ cat nonexistent-file.txt
Working Directory: The current working directory.
Output: An error message - "No such file or directory."
Explanation: If you attempt to cat a file that doesn't exist, you'll receive an error because the specified file is not found in the filesystem.

Conclusion:
These are the basic filesystem commands that we covered in this lab. Understanding how to use cd, ls, and cat is essential for effective navigation and manipulation of files and directories in a Unix-based system.
