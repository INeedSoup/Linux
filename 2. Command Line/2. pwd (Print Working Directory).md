### Understanding the Linux Filesystem

Linux organizes everything inside a single hierarchical structure known as the filesystem.  
Everything starts from the root directory, written as `/`.  
From there, the system branches into multiple subdirectories, and those can contain more folders and files.

Example of a simplified directory tree:

```
/
|-- bin
|   |-- file1
|   |-- file2
|-- etc
|   |-- file3
|   `-- directory1
|       |-- file4
|       `-- file5
|-- home
|-- var
```

---

## Understanding File Paths

A path describes where a file or folder is located.

### Absolute Path

- Starts from `/` and shows the complete route.    
- Example:      
```
/home/pete/Movies
```

### Relative Path

- Based on your current working directory.    
- Does not start with `/`.    

---

## What `pwd` Means

`pwd` stands for **print working directory**.  
It shows the full absolute path of the directory you are currently in.

---

## Using `pwd`

To check your exact location in the filesystem, run:

```
pwd
```

The output will look something like:

```
/home/pete/Documents
```

This helps you stay oriented while navigating with commands like `cd`.
