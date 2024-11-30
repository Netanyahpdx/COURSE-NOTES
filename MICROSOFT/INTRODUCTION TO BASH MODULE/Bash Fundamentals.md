# BASH FUNDAMENTALS#
  
An understanding of Bash starts with an understanding of Bash syntax. After you know the syntax, you can apply it to every Bash command you run.  
    
The full syntax for a Bash command is:  
![image](https://github.com/user-attachments/assets/bfdb0f04-d7bc-423f-9a97-62fafcf3afd4)  
  
Bash treats the first string it encounters as a command. The following command uses Bash's ls (for "list") command to display the contents of the current working directory:  
![image](https://github.com/user-attachments/assets/856ff098-d98b-481c-907b-bf97cd27451b)  
  
Arguments often accompany Bash commands. For example, you can include a path name in an ls command to list the contents of another directory:  
![image](https://github.com/user-attachments/assets/648acc1b-a508-4537-a726-70f64b3fd6ae)  
  
Most Bash commands have options for modifying how they work. Options, also called flags, give a command more specific instructions. As an example, files and directories whose names begin with a period are hidden from the user and aren't displayed by ls. However, you can include the -a (for "all") flag in an ls command and see everything in the target directory: 
![image](https://github.com/user-attachments/assets/23dd7235-dd4d-4934-b99b-b3ae6e8cf2d5)  
  
You can even combine flags for brevity. For example, rather than enter ls -a -l /etc to show all files and directories in Linux's /etc directory in long form, you can enter this instead:  
![image](https://github.com/user-attachments/assets/3efe97f7-2c30-4051-8b62-6e9b446fe5a8)  
Bash is concise. It's sometimes remarkable (and a point of pride among Bash aficionados) how much you can accomplish with a single command.

---

**GET HELP**  
Which options and arguments can be used, or must be used, varies from command to command. Fortunately, Bash documentation is built into the operating system. Help is never more than a command away. To learn about the options for a command, use the man (for "manual") command. For instance, to see all the options for the mkdir ("make directory") command, do this:  
![image](https://github.com/user-attachments/assets/19ef95d4-1f3e-4e88-9e3a-f92aebaa8ede)  
man is your best friend as you learn Bash. man is how you find the information you need to understand how any command works.  

Most Bash and Linux commands support the --help option. This shows a description of the command's syntax and options. To demonstrate, enter mkdir --help. The output looks something like this:
![image](https://github.com/user-attachments/assets/ab78f875-bfbc-4454-8cfa-162574411317)  
Help obtained this way is typically more concise than help obtained with man.  
  
---

**USE WILDCARDS**  
Wildcards are symbols that represent one or more characters in Bash commands. The most frequently used wildcard is the asterisk. It represents zero characters or a sequence of characters. Suppose your current directory contains hundreds of image files, but you only want to see the PNG files; the ones whose file names end with .png. Here's the command to list only those files:  
![image](https://github.com/user-attachments/assets/2939c0d8-7858-422f-b191-e22e4c84a4df)    
NOTE: Linux has no formal concept of a file-name extension as other operating systems do. This doesn't mean that PNG files won't have a .png extension. It simply means Linux attaches no special significance to the fact that the file names end with .png.  
 
Now let's say the current directory also contains JPEG files. Some end in .jpg, while others end in .jpeg. Here's one way to list all the JPEG files:  
![image](https://github.com/user-attachments/assets/af8393ed-86e5-4d84-8661-867980c31100)   
  
And here's another:  
![image](https://github.com/user-attachments/assets/d8fe7b4d-0316-4da7-b1e9-2baa93e41532)  
  
The * wildcard matches on zero or more characters, but the ? wildcard represents a single character. If the current directory contains files named 0001.jpg, 0002.jpg, and so on through 0009.jpg, the following command lists them all:  
![image](https://github.com/user-attachments/assets/0eab6a19-cc94-4eeb-b6d5-c8b6c294962c)   
  
Yet another way to use wildcards to filter output is to use square brackets, which denote groups of characters. The following command lists all the files in the current directory whose names contain a period immediately followed a lowercase J or P. It lists all the .jpg, .jpeg, and .png files, but not .gif files:  
![image](https://github.com/user-attachments/assets/c0929a79-d13a-4e7a-a324-05b7a36acb9b)  
  
In Linux, file names and the commands that operate upon them are case-sensitive. So to list all the files in the current directory whose names contain periods followed by an uppercase or lowercase J or P, you could enter this:  
![image](https://github.com/user-attachments/assets/fcd9a372-a918-464b-9743-f6e8a4b00a7d)  
   
Expressions in square brackets can represent ranges of characters. For example, the following command lists all the files in the current directory whose names begin with a lowercase letter:  
![image](https://github.com/user-attachments/assets/a14b2b35-b062-487a-8cd3-72633d678e26)  
  
This command, by contrast, lists all the files in the current directory whose names begin with an uppercase letter:  
![image](https://github.com/user-attachments/assets/900f76b7-8761-41fd-b627-628a43624531)  
  
And this one lists all the files in the current directory whose names begin with a lowercase or uppercase letter:  
![image](https://github.com/user-attachments/assets/cb82656a-0b52-4ec1-8ce8-cf13f1aee30a)  
   
Based on all this, can you guess what the following commands do?  
![image](https://github.com/user-attachments/assets/70ffb21d-825c-40d0-a804-ef2a782c50d9)  
  
If you need to use one of the wildcard characters as an ordinary character, you make it literal or "escape it" by prefacing it with a backslash. So, if for some reason you had an asterisk as part of a file name—something you should never do intentionally—you could search for it by using a command such as:  
![image](https://github.com/user-attachments/assets/e64e24b4-532d-48f3-9d30-e9822480c62c)  
  


# Bash Syntax and Commands: Input vs. Expected Output

| **Input**                       | **Expected Output/Outcome**                                                                                       |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `command [options] [arguments]` | Basic Bash command structure.                                                                                     |
| `ls`                            | Lists the contents of the current directory.                                                                      |
| `ls /etc`                       | Lists the contents of the `/etc` directory.                                                                       |
| `ls -a /etc`                    | Lists all files (including hidden ones) in the `/etc` directory.                                                  |
| `ls -al /etc`                   | Lists all files (including hidden ones) in the `/etc` directory in long format.                                   |
| `man mkdir`                     | Opens the manual page for the `mkdir` command. Provides detailed information about its options and usage.         |
| `mkdir --help`                  | Displays help information for the `mkdir` command with a list of options and brief descriptions.                  |
| `ls *.png`                      | Lists all files in the current directory with a `.png` extension.                                                 |
| `ls *.jpg *.jpeg`               | Lists all files in the current directory with `.jpg` or `.jpeg` extensions.                                       |
| `ls *.jp*g`                     | Lists all files in the current directory matching `.jpg` and `.jpeg` extensions (using wildcard).                |
| `ls 000?.jpg`                   | Lists all `.jpg` files in the current directory with names matching `0001.jpg`, `0002.jpg`, etc., up to `0009.jpg`.|
| `ls *.[jp]*`                    | Lists all files in the current directory ending with `.jpg`, `.jpeg`, or `.png`.                                  |
| `ls *.[jpJP]*`                  | Lists all files in the current directory ending with `.jpg`, `.jpeg`, `.JPG`, `.JPEG`, or `.PNG`.                 |
| `ls [a-z]*`                     | Lists all files in the current directory whose names begin with a lowercase letter.                               |
| `ls [A-Z]*`                     | Lists all files in the current directory whose names begin with an uppercase letter.                              |
| `ls [a-zA-Z]*`                  | Lists all files in the current directory whose names begin with any letter, uppercase or lowercase.               |
| `ls [0-9]*`                     | Lists all files in the current directory whose names begin with a digit.                                          |
| `ls *[0-9]*`                    | Lists all files in the current directory containing at least one digit in their name.                             |
| `ls *[0-9]`                     | Lists all files in the current directory ending with a digit.                                                     |
| `ls *\**`                       | Searches for files with an asterisk (`*`) in their name, escaping the wildcard.                                   |








