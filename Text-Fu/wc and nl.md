These two commands help you inspect and analyze text files. **wc** focuses on counting, while **nl** adds line numbers for easier reading.

---

## **wc (Word Count)**

### **Purpose**

Provides basic statistics about a file:

- number of lines    
- number of words    
- number of bytes    

### **Basic Usage**

```
wc /etc/passwd
```

Example output:

```
 96     265    5925 /etc/passwd
```

Meaning:

1. **96** lines    
2. **265** words    
3. **5925** bytes    
4. Filename    

---

### **Getting Specific Counts**

You can request only one type of count:

- `-l` : line count    
```
wc -l /etc/passwd
```
- `-w` : word count    
```
wc -w notes.txt
```
- `-c` : byte count
```
wc -c data.bin
```
- `-m` : character count (useful for UTF-8 text)
```
wc -m story.txt
```

The output becomes simpler when using specific options.

---

## **nl (Number Lines)**

### **Purpose**

Adds line numbers to the beginning of each line of a file. This is useful when reading scripts, logs, or configuration files.

### **Example File** (file1.txt)

```
i
like
turtles
```

Command:

```
nl file1.txt
```

Output:

```
     1 i
     2 like
     3 turtles
```

The numbering is right-aligned by default, and nl gives you more control than cat -n, especially for numbering blank lines or handling formatting.

---

## **Extra Options Worth Knowing**

### **nl**

- `-b a` : number all lines, including blank ones
- `-b t` : number only non-empty lines (default behavior)
- `-n rz` : pad line numbers with leading zeros

### **wc**

- Works with pipelines:
```
cat file.txt | wc -l
```
- Combine with grep to count matches:
```
grep "error" log.txt | wc -l
```