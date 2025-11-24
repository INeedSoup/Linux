### What `ls` Does
`ls` lists the files and directories inside a given location.  
If you don’t provide a path, it shows the contents of your current directory.

Examples:

```
ls
ls /home/pete
```

---

## Viewing Hidden Files

Linux hides files and folders whose names start with a dot.  
To see everything, including hidden items:

```
ls -a
```

---

## Showing Detailed Information

Use the long format option to see extra details such as:

- Permissions    
- Number of links    
- Owner    
- Group    
- File size    
- Last modification time    
- File or directory name    

Command:

```
ls -l
```

Example output:

```
drwxr-x--- 7 pete penguingroup 4096 Nov 20 16:37 Desktop
```

---

## Reverse Sorting

If you want to reverse the default sort order (usually alphabetical):

```
ls -r
```

This is helpful if you want to see the last items first.

---

## Combining Flags

You can combine multiple options in one command. Order doesn’t matter.

Examples:

```
ls -la
ls -al
ls -lar
```

`-l` = long format  
`-a` = show all files  
`-r` = reverse sort
