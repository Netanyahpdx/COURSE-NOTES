# BASH COMMANDS & OPERATORS #

Every shell language has its most used commands. Let's start building your Bash repertoire by examining the most commonly used commands.

---

**BASH COMMANDS**

ls command  
ls lists the contents of your current directory or the directory specified in an argument to the command. By itself, it lists the files and directories in the current directory:   
![image](https://github.com/user-attachments/assets/c491de92-08c3-42d8-b377-4a00b6dfd9af)  
  
Files and directories whose names begin with a period are hidden by default. To include these items in a directory listing, use an -a flag:  
![image](https://github.com/user-attachments/assets/236d8dae-1adf-48ee-8626-60aeb717f39f)  
  
To get even more information about the files and directories in the current directory, use an -l flag:  
![image](https://github.com/user-attachments/assets/23a07042-24ae-40ce-9d47-dfb9f3b0d371)  
  
Here's some sample output from a directory that contains a handful of JPEGs and PNGs and a subdirectory named gifs:  
![image](https://github.com/user-attachments/assets/50c7e2d0-f6f3-46c2-b4d3-f20179bde03e)  
Each line provides detailed information about the corresponding file or directory. That information includes the permissions assigned to it, its owner, its size in bytes, the last time it was modified, and the file or directory name.  

---

**cat COMMAND**  
   
Suppose you want to see what's inside a file. You can use the cat command for that. The output won't make much sense unless the file is a text file. The following command shows the contents of the os-release file stored in the /etc directory:  
![image](https://github.com/user-attachments/assets/7d49da96-1c33-4c2e-8a13-aa43d0bea1f0)   
This is a useful command because it tells you which Linux distribution you're running:   
![image](https://github.com/user-attachments/assets/953acd8f-5b40-4fb5-8d63-0eb5c41458be)  
The /etc directory is a special one in Linux. It contains system-configuration files. You don't want to delete any files from this directory unless you know what you're doing.  
  
---

**sudo COMMAND**  

Some Bash commands can only be run by the root user; a system administrator or superuser. If you try one of these commands without sufficient privileges, it fails. For example, only users logged in as a superuser can use cat to display the contents of /etc/at.deny:  
![image](https://github.com/user-attachments/assets/26226c2d-b58b-4372-966c-49f692733e2b)  
at.deny is a special file that determines who can use other Bash commands to submit jobs for later execution.  
  
You don't want to run as root most of the time; it's too dangerous. To run commands that require admin privilege without logging in as a superuser, you'll preface the commands with sudo:  
![image](https://github.com/user-attachments/assets/172d407e-ee67-458f-82c0-8eacad5ffbc7)  
sudo stands for "superuser do." When you use it, you're telling the shell that for this one command, you're acting with the root-user level of permission.  
  
---
  
**cd, mkdir, rmdir COMMANDS**  
  
cd stands for "change directory," and it does exactly what the name suggests: it changes the current directory to another directory. It enables you to move from one directory to another just like its counterpart in Windows. The following command changes to a subdirectory of the current directory named orders:  
![image](https://github.com/user-attachments/assets/b84af671-03ac-4cfc-b9f6-7a05e9e518a3)  
  
You can move up a directory by specifying .. as the directory name:  
![image](https://github.com/user-attachments/assets/c5d4fdd4-5e63-4974-80eb-f1127a653255)  
   
This command changes to your home directory; the one you land in when you first sign in:  
![image](https://github.com/user-attachments/assets/848b0b22-a90c-4c17-9e80-8cb6e9d31d8e)  
  
You can create directories by using the mkdir command. The following command creates a subdirectory named orders in the current working directory:  
![image](https://github.com/user-attachments/assets/15e06e60-ca41-44eb-88e7-c73b7f1c040b)  
    
If you want to create a subdirectory and another subdirectory under it with one command, use the --parents flag:  
![image](https://github.com/user-attachments/assets/1922b4eb-d3bd-4e2a-8141-b4d66a5af719)  
    
---
  
**rm COMMAND**

The rmdir command deletes (removes) a directory, but only if it's empty. If it's not empty, you get a warning instead. Fortunately, you can use the rm command to delete directories that aren't empty in combination with the -r (recursive) flag. The command would then look like so, rm -r.  
  
The rm command is short for "remove." As you'd expect, rm deletes files. So this command puts an end to 0001.jpg:  
![image](https://github.com/user-attachments/assets/29adf8d2-fafb-435e-bc1b-e46cb007463e)  

And this command deletes all the files in the current directory:  
![image](https://github.com/user-attachments/assets/4e3bd7eb-6fa2-4dda-a290-72579b8296da)  
  
Be wary of rm. It's a dangerous command.  
  
Running rm with a -i flag lets you think before you delete:  
![image](https://github.com/user-attachments/assets/2dd0e0c7-bc63-474e-b29c-8a5e8de512f1)  
  
Make it a habit to include -i in every rm command, and you might avoid falling victim to one of Linux's biggest blunders. The dreaded rm -rf / command deletes every file on an entire drive. It works by recursively deleting all the subdirectories of root and their subdirectories. The -f (for "force") flag compounds the problem by suppressing prompts. Don't do this.  
   
If you want to delete a subdirectory named orders that isn't empty, you can use the rm command this way:
![image](https://github.com/user-attachments/assets/c2523af8-5cf0-4807-b9ac-dc8cc4b792ce)  
This deletes the orders subdirectory and everything in it, including other subdirectories.

---
  
**cp COMMAND**  
  
The cp command copies not just files, but entire directories (and subdirectories) if you want. To make a copy of 0001.jpg named 0002.jpg, use this command:  
![image](https://github.com/user-attachments/assets/8ee2da72-e39b-4e59-af76-69a9f9695425)  
  
If 0002.jpg already exists, Bash silently replaces it. That's great if it's what you intended, but not so wonderful if you didn't realize you were about to overwrite the old version.  
  
Fortunately, if you use the -i (for "interactive") flag, Bash warns you before deleting existing files. This is safer:  
![image](https://github.com/user-attachments/assets/d229f575-dc84-4fa7-a6bf-f9cd70974f3e)  
  
You can use wildcards to copy several files at once. To copy all the files in the current directory to a subdirectory named photos, do this:  
![image](https://github.com/user-attachments/assets/49e4339e-4c17-44ee-9e2f-7f86c609c924)  
  
To copy all the files in a subdirectory named photos into a subdirectory named images, do this:  
![image](https://github.com/user-attachments/assets/eb7301c1-52ca-4022-87fb-ee5bc3768c8a)  
  
This assumes that the images directory already exists. If it doesn't, you can create it and copy the contents of the photos directory by using this command:  
![image](https://github.com/user-attachments/assets/60879831-8f11-42fa-96ff-28356af2dd78)  
  
The -r stands for "recursive." An added benefit of the -r flag is that if photos contains subdirectories of its own, they too are copied to the images directory.  

---

**ps COMMAND**

The ps command gives you a snapshot of all the currently running processes. By itself, with no arguments, it shows all your shell processes; in other words, not much. But it's a different story when you include a -e flag:  
![image](https://github.com/user-attachments/assets/0800eb54-a97e-4a11-aa71-eeac4fd6708e)  
-e lists all running processes, and there are typically many of them.  
   
For a more comprehensive look at what processes are running in the system, use the -ef flag:  
![image](https://github.com/user-attachments/assets/2ca4bb29-21b1-48ca-827b-fc4c5ca06971)  
  
This flag shows the names of all the running processes, their process identification numbers (PIDs), the PIDs of their parents (PPIDs), and when they began (STIME). It also shows what terminal, if any, they're attached to (TTY), how much CPU time they've racked up (TIME), and their full path names. Here's an abbreviated example:  
![image](https://github.com/user-attachments/assets/84b8cb49-9726-434c-a40c-0cd0737bf0a2)  
  
As an aside, you might find documentation that shows ps being used this way:  
![image](https://github.com/user-attachments/assets/1b0ffa8e-ea3a-49e2-a99e-4700605f7de7)  
  
ps aux and ps -ef are the same. This duality traces back to historical differences between POSIX Unix systems (of which Linux is one) and BSD Unix systems (the most common of which is macOS). In the beginning, POSIX used -ef while the BSD required aux. Today, both operating-system families accept either format.  
  
This serves as an excellent reminder of why you should look closely at the manual for all Linux commands. Learning Bash is like learning English as a second language. There are many exceptions to the rules.  

---

**w COMMAND**  
  
Users come, users go, and sometimes you get users you don't want at all. When an employee leaves to pursue other opportunities, the sysadmin is called upon to ensure that the worker can no longer sign in to the company's computer systems. Sysadmins are also expected to know who's logged in, and who shouldn't be.  
  
To find out who's on your servers, Linux provides the w (for "who") command. It displays information about the users currently on the computer system and those users' activities. w shows user names, their IP addresses, when they logged in, what processes they're currently running, and how much time those processes are consuming. It's a valuable tool for sysadmins.  
   
---

**BASH I/O OPERATORS**  
  
You can do a lot in Linux just by exercising Bash commands and their many options. But you can really get work done when you combine commands by using I/O operators:  
  
- < for redirecting input to a source other than the keyboard  
- > for redirecting output to destination other than the screen  
- >> for doing the same, but appending rather than overwriting  
- | for piping output from one command to the input of another  
  
Suppose you want to list everything in the current directory but capture the output in a file named listing.txt. The following command does just that:  
![image](https://github.com/user-attachments/assets/94d96d94-4c01-4c07-82e5-58cb06d05d93)  
  
If listing.txt already exists, it gets overwritten. If you use the >> operator instead, the output from ls is appended to what's already in listing.txt:  
![image](https://github.com/user-attachments/assets/7d7edc59-59d0-43b5-8f58-99220a66930d)  
  
The piping operator is powerful (and often used). It redirects the output of the first command to the input of the second command. Let's say you use cat to display the contents of a large file, but the content scrolls by too quickly for you to read. You can make the output more manageable by piping the results to another command such as more. The following command lists all the currently running processes. But once the screen is full, the output pauses until you select Enter to show the next line:  
![image](https://github.com/user-attachments/assets/eb7c9ec2-f4f8-40b9-8ee6-ff529bc4d55d)  
  
You can also pipe output to head to see just the first several lines:  
![image](https://github.com/user-attachments/assets/af264b2f-87a1-4dfb-ba4e-e4e1e17399d8)  
  
Or suppose you want to filter the output to include only the lines that contain the word "daemon." One way to do that is by piping the output from ps to Linux's useful grep tool:
![image](https://github.com/user-attachments/assets/0c34e737-61cd-4fb9-b980-d8f06c662bdf)  
  
The output might look like this:   
![image](https://github.com/user-attachments/assets/3b1e9222-450f-4904-9477-9b7c10822c3e)  
  
You can also use files as input. By default, standard input comes from the keyboard, but it too can be redirected. To get input from a file instead of the keyboard, use the < operator. One common sysadmin task is to sort the contents of a file. As the name suggests, sort sorts text in alphabetical order:  
![image](https://github.com/user-attachments/assets/c51bd769-c5cd-4468-97e7-4e8468b7f8f4)  
  
To save the sorted results to a new file, you can redirect input and output:  
![image](https://github.com/user-attachments/assets/9db7cf06-40ab-4584-b918-df499cb84202)  
  
You can use I/O operators to chain Linux commands as needed. Consider the following command:  
![image](https://github.com/user-attachments/assets/81dac59e-37a9-483c-a3d2-67c1d0351028)  
  
The output from cat goes to fmt, the output from fmt goes to pr, and so on. fmt formats the results into a tidy paragraph. pr paginates the results. And lpr sends the paginated output to the printer. All in a single line!  



























