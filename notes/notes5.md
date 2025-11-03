# Linux Commands, Variables, and Directory Concepts

## Commands

### **ls**
- **Definition:** Lists files and directories in the current or specified directory.  
- **Formula:** `ls [options] [directory]`  
- **Examples:**
  - `ls /home/user/Documents`

### **pwd**
- **Definition:** Prints the current working directory.  
- **Formula:** `pwd`  
- **Examples:**
  - `pwd`
  - Output: `/home/user/Desktop`

### **cd**
- **Definition:** Changes the current directory.  
- **Formula:** `cd [directory]`  
- **Examples:**
  - `cd /home/user/Documents`


A **variable** is a name used to store data that can be reused or moddified.
You can call it with `$`.  
Example:  
`name="Alex"`  
`echo $name`

An **environment variable** is a variable that affects how processes or programs run.  
Example:  
`echo $PATH`  
`export PATH=$PATH:/new/path`

A **user defined variable** is a variable created by the user. 
Example:  
`myVar="Hello"`  
`echo $myVar`

The **root directory** is the top-level directory in Linux, represented by `/`.

The **Parent Directory** is the directory that contains another directory.

The **Current Working Directory** is the directory you are currently in, can be shown using `pwd`.

An **absolute path** is a complete path starting from the root. Example: `~/home/user/Documents/file.txt`  

A **relative path** starts from your location. Example: `../Downloads/file.txt`

The difference between **Your home directory** and **The home directory** is that *your home directory* refers to your personal folder (e.g., `/home/alex`), while *the home directory* refers to the main directory that contains all users’ home folders (e.g., `/home`).