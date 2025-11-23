The `head` command is useful when you want to quickly inspect the beginning of a file without opening it in an editor or scrolling through pages of text.

This is especially helpful for large files like system logs.

---

## **Default Behavior**

### **Shows the first 10 lines**

```
head /var/log/syslog
```

- Prints the first 10 lines of the file.    
- Gives a quick snapshot of what the file contains.    

---

## **Customizing the Line Count**

### **Use `-n` to specify how many lines to show**

```
head -n 15 /var/log/syslog
```

- Displays the first 15 lines instead of the default 10.    
- You can choose any number you need.    

Example:

```
head -n 3 file.txt
```

---

## **When head is useful**

- Previewing logs    
- Checking file headers    
- Verifying output from scripts or commands    
- Inspecting configuration files without opening the whole thing    
