### **What stdin is**

- stdin is the default input stream for commands.    
- Most programs read their input from the keyboard unless told otherwise.    
- stdin and stdout work together:    
    - **stdin** supplies data to a program        
    - **stdout** displays or outputs the result        

Understanding both is key to working smoothly in the shell.

---

## **Redirecting stdin with `<`**

### **Purpose of `<`**

- The `<` operator tells a command to take its input from a file instead of the keyboard.   
- This is often used when you want a command to operate on the contents of a file without typing anything manually.    

Example:

```
command < file
```

The file becomes the input to the command.

---

## **Example: Using cat with stdin and stdout**

```
cat < peanuts.txt > banana.txt
```

### **What happens step by step**

1. `< peanuts.txt`  
    The cat command reads its stdin from the file peanuts.txt.    
2. `cat`  
    It processes that input. Cat simply outputs whatever it reads.    
3. `> banana.txt`  
    The output of cat (stdout) goes to banana.txt. If the file exists, it is overwritten.    

### **Result**

- The contents of peanuts.txt are copied into banana.txt.    
- You used both stdin and stdout redirection in a single command.    

---

## **Why stdin redirection matters**

- It allows commands to operate on files silently, without manual typing.    
- It is essential for automation, scripting, and chaining commands.    
- It becomes especially powerful when combined with stdout redirection or pipes.    
