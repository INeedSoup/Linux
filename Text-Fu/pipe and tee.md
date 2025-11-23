### **Why pipes matter**

The real power of the Linux command line comes from taking the output of one command and feeding it directly into another. This lets you build small, simple commands into powerful workflows.

---

## **The Pipe Operator `|`**

### **What a pipe does**

- A pipe takes **stdout** from the command on the left and sends it as **stdin** to the command on the right.
- This avoids creating temporary files and keeps your workflow efficient.
   Example:

```
ls -la /etc | less
```

- `ls -la /etc` lists many files.    
- `less` lets you scroll through the output.    
- The pipe connects them so you can view the output interactively.    

### **When pipes are useful**

- Browsing long output    
- Filtering text with commands like grep, sort, uniq, wc    
- Passing data through multiple steps    

---

## **The tee Command**

### **What tee does**

`tee` splits output into two paths:

1. Sends it to your terminal (stdout)    
2. Saves it to a file    

Example:

```
ls | tee peanuts.txt
```

- You still see the output on the screen.    
- A copy is written to peanuts.txt.    

This is very useful for logging, debugging, and monitoring.

### **Appending with tee**

Like redirection, tee can append using `-a`:

```
ls | tee -a peanuts.txt
```

---

## **Using pipes with tee**

You can place tee in the middle of a pipeline to save intermediate data while continuing to process it.

Example:

```
ls -la /etc | tee etc_listing.txt | grep "conf"
```

What happens:

1. `ls -la /etc` lists everything in /etc.    
2. `tee` saves a copy to etc_listing.txt and passes the same output forward.    
3. `grep "conf"` filters for lines containing “conf”.    

This pattern is common when you want to log data but still use it in further commands.

---

## **Why pipes and tee matter**

- They help you avoid unnecessary files.    
- They make your command chains faster and cleaner.    
- They create flexible workflows for processing, filtering, and saving data.    
- They’re essential for automation and scripting.