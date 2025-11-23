The `paste` command merges lines from a file. It works similarly to `cat`, but instead of printing lines one after another, it joins them horizontally.

You created a file:

**sample2.txt**

```
The
quick
brown
fox
```

---

## **Merging Lines with `-s`**

### **`-s` (serial mode)**

- Joins all lines into a single line.    
- Uses TAB as the default delimiter.    

Example:

```
paste -s sample2.txt
```

Output becomes one line, with TABs between each word.

---

## **Changing the Delimiter (`-d`)**

### **Using a custom delimiter**

You can replace the default TAB with any character.

Example:

```
paste -d ' ' -s sample2.txt
```

This uses a space as the delimiter, producing:

```
The quick brown fox
```

---

## **When paste is useful**

- Joining columns or lines into a single line    
- Creating quick one-line summaries    
- Preparing data for scripts or reports    
- Combining multiple files side by side    