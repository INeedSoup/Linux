### **What stderr is**

- stderr is the default stream used for error messages and diagnostics.    
- It is separate from stdout, which handles normal command output.    
- Both stdout and stderr usually appear on your terminal, which is why errors show up even when you redirect stdout.    

Example:

```
ls /fake/directory > peanuts.txt
```

You still see the error because it comes from stderr, not stdout.

---

## **File Descriptors**

Linux identifies the standard streams with numbers called file descriptors:

- **0** – stdin    
- **1** – stdout    
- **2** – stderr    

These numbers let you control where each stream goes.

---

## **Redirecting stderr**

### **Send only stderr to a file**

```
ls /fake/directory 2> peanuts.txt
```

- `2>` sends file descriptor 2 (stderr) to peanuts.txt.    
- Errors go into the file, not the terminal.    

---

## **Combining stdout and stderr**

### **Method 1: Traditional form**

```
ls /fake/directory /etc/passwd > peanuts.txt 2>&1
```

Explanation:

1. `> peanuts.txt` redirects stdout.    
2. `2>&1` sends stderr to wherever stdout is currently going.  
    Since stdout is going to peanuts.txt, stderr goes there too.    

Order matters. If you reverse them, you don't get the same result.

---

### **Method 2: Modern shortcut**

```
ls /fake/directory /etc/passwd &> peanuts.txt
```

- `&>` redirects both stdout and stderr to the same file.    
- Works in bash and many other shells.    

---

## **Discarding error messages**

Sometimes you want to ignore errors completely.  
Redirect stderr to `/dev/null`, the “black hole” of Linux.

```
ls /fake/directory 2> /dev/null
```

- stderr disappears    
- stdout (if any) is still shown normally    

---

## **Why stderr matters**

- It keeps error messages separate from regular output.   
- It helps you debug commands more easily.    
- It lets you control logs properly when automating or scripting.