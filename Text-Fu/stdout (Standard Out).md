### **What stdout is**

- Most Linux commands send their output to a default stream called **standard output**, or **stdout**.    
- stdout usually appears directly on your terminal screen.    
- Commands interact with three main I/O streams:    
    - **stdin** – input to a command        
    - **stdout** – normal output from a command        
    - **stderr** – error messages (not covered here but useful to know)        

Example:

```
echo Hello World
```

This prints the text to your terminal because the output goes to stdout.

---

## **Redirecting stdout**

### **1. Overwriting output with `>`**

- The `>` operator redirects stdout to a file.    
- If the file doesn’t exist, it is created.    
- If the file exists, its contents are **replaced**.    

Example:

```
echo Hello World > peanuts.txt
```

This creates or replaces the file `peanuts.txt` with the text "Hello World".

### **Important note**

- Redirecting with `>` is destructive if the file already has data.    
- Always double-check before using it on important files.    

---

## **2. Appending output with `>>`**

- The `>>` operator adds new output to the end of an existing file.    
- If the file doesn’t exist, it is created.    
- This is safer when you want to keep previous content.    

Example:

```
echo Hello World >> peanuts.txt
```

This adds “Hello World” to the end of the file instead of overwriting it.

---

## **Why stdout redirection matters**

- It lets you save command output into files.    
- It helps you log information for later use.    
- It is a core skill for shell scripting and automation.    
- It helps you separate input, output, and errors for cleaner workflows.    
