Tabs and spaces can cause formatting issues because different editors display tabs differently. Linux provides two simple tools to convert between them: `expand` and `unexpand`.

---

## **expand — Converting Tabs to Spaces**

### **Basic usage**

```
expand sample.txt
```

- Reads the file.    
- Replaces each tab with spaces.    
- Prints the result to the terminal.    

### **Default behavior**

- Each tab becomes **8 spaces** unless you specify otherwise.    

### **Saving the output**

`expand` does not change the file automatically.  
To save the converted text:

```
expand sample.txt > result.txt
```

This writes a new version of the file with spaces instead of tabs.

---

## **unexpand — Converting Spaces to Tabs**

### **Basic usage**

```
unexpand -a result.txt
```

- Converts spaces back into tabs.    
- Useful for reducing file size or following coding styles that use tabs.    

### **Default behavior**

- Without `-a`, `unexpand` only converts **leading spaces**.    
- With `-a`, it converts **all** sequences of spaces that match tab stops.    

---

## **When these commands are useful**

- Cleaning up inconsistent indentation    
- Preparing text for editors that treat tabs differently    
- Converting between formatting styles for scripts or code    
- Reducing file size in large, indented files
  