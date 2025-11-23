The `cut` command extracts specific parts of lines from a text file. It can select characters or fields, depending on the options you use.

Before trying the examples, you created a file:

```
echo 'The quick brown; fox jumps over the lazy  dog' > sample.txt
```

(Remember: there is a **TAB** between “lazy” and “dog”.)

---

## **Cutting by Character (`-c`)**

### **How it works**

- The `-c` option extracts characters by their position.    
- Spaces count as characters.    

Example:

```
cut -c 5 sample.txt
```

This prints the 5th character of the line.  
For sample.txt, the output is:

```
q
```

---

## **Cutting by Field (`-f`)**

### **How fields work**

- By default, `cut` treats **TAB** as the delimiter.    
- Each TAB-separated segment is a field.    

Example:

```
cut -f 2 sample.txt
```

Because there is a TAB between “lazy” and “dog”, the second field is:

```
dog
```

---

## **Using Custom Delimiters (`-d`)**

You can change the delimiter with the `-d` option.

Example:

```
cut -f 1 -d ";" sample.txt
```

Here’s what happens:

- The delimiter is set to `;`    
- The command extracts field 1    
- The text before the semicolon is:    

```
The quick brown
```

---

## **When to use cut**

- Extracting columns from CSV, TSV, or logs    
- Pulling out specific character ranges    
- Cleaning or preprocessing text before passing it to other commands    

---

If you want, I can add notes for `awk`, `sed`, or other text processing tools next.