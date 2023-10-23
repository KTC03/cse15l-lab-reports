# Lab 1: Remote Access and FileSystem

In this lab report, I go through some fundamental filesystem commands, specifically cd, ls, and cat. We'll explore how these commands work with various arguments and scenarios.

### cd Command
1: Using cd with No Arguments

![Image](1.png)

- Working Directory: /home
- Output: No output
- Explanation: Running cd without any arguments takes you to your home directory. 

2: Using cd with a Directory Path

![Image](4.png)

- Working Directory: /home
- Output: No output.
- Explanation: When you use cd with a directory path, you change your working directory to the specified directory. In this case, we navigated to Lecture1.

Example 3: Using cd with a File Path

![Image](8.png)

- Working Directory: /home
- Output: An error message - "Not a directory"
- Explanation: If you attempt to use cd with a path to a file, you'll receive an error because the cd command is designed to change directories, not files. This error message indicates that the specified path is not a directory and cannot be used with cd.

### ls Command
1: Using ls with No Arguments

![Image](2.png)

- Working Directory: /home
- Output: List of files/directories in the current working directory - in this instance the directory Lecture1 is shown.
- Explanation: Running ls without arguments will display the contents of the current working directory. This is a quick way to see what's in the directory you're in.

2: Using ls with a Directory Path

![Image](5.png)

- Working Directory: /home
- Output: List of files and directories in the specified directory - in this instance the specified directory is Lecture1 
- Explanation: When you use ls with a directory path, it shows the contents of the specified directory without changing your working directory.

3: Using ls with a File Path

![Image](7.png)

- Working Directory: /home
- Output: An error message - "No such file or directory"
- Explanation: When you use ls with a file path, you'll receive an error because the ls command is meant to list the contents of directories, not individual files. It expects a directory path as an argument. If you specify a file path, you'll get an error message indicating that the file or directory does not exist.

### cat Command
1: Using cat with No Arguments

![Image](3.png)

- Working Directory: /home
- Output: No output
- Explanation: Running cat without any arguments is incorrect as it expects a file to be specified. Hence, it's an error.

2: Using cat with a Directory Path

![Image](6.png)

- Working Directory: /home
- Output: An error message - "Is a directory"
- Explanation: When you use cat with a directory path, you'll receive an error because cat is designed to display the content of files, not directories. This error message indicates that you cannot use cat to display the contents of a directory.

3: Using cat with a File Path

![Image](9.png)

- Working Directory: /home
- Output: The content of the "Hello.java" file.
- Explanation: When you use cat with a file path, it displays the content of the specified file. 
