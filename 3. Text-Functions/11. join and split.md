Working with text files is a routine part of Linux usage. Two useful commands for this are **join**, used for merging lines from files based on a shared field, and **split**, used for breaking large files into smaller pieces.

---

## **join Command**

### **Purpose**

Merges lines from two files based on a common field. Useful when you want to combine related data stored in separate text files.

### **Basic Requirements**

- Both files must be sorted on the join field.    
- By default, join matches the first field of each file.    

### **Example: Default Behavior**

file1.txt

```
1 John
2 Jane
3 Mary
```

file2.txt

```
1 Doe
2 Doe
3 Sue
```

Command:

```
join file1.txt file2.txt
```

Output:

```
1 John Doe
2 Jane Doe
3 Mary Sue
```

### **Joining Using Different Fields**

If the matching fields are not in the first column, you can specify which field to use.

Example files:

file1.txt

```
John 1
Jane 2
Mary 3
```

file2.txt

```
1 Doe
2 Doe
3 Sue
```

Command:

```
join -1 2 -2 1 file1.txt file2.txt
```

- `-1 2` tells join to use field 2 of file1   
- `-2 1` tells join to use field 1 of file2    

Output:

```
1 John Doe
2 Jane Doe
3 Mary Sue
```

### **Other Useful Options**

- `-t` : Specify a different field delimiter (comma, colon, etc.)    
- `-a` : Include unpairable lines from one or both files    
- `-v` : Show only unpairable lines    
- `-i` : Case-insensitive matching    

---

## **split Command**

### **Purpose**

Breaks a large file into smaller files. Useful for handling big logs, backups, or when transferring data in parts.

### **Basic Usage**

```
split somefile
```

- Splits the input file into chunks of **1000 lines** each.    
- Output files are named **xaa**, **xab**, **xac**, and so on.    

### **Useful Options**

- `-l <num>` : Split by number of lines   
```
split -l 2000 largefile
```
	Creates chunks of 2000 lines each.
- `-b <size>` : Split by file size
```
split -b 10M largefile
```
	   Creates files of 10 MB each.
- `-d` : Use numeric suffixes instead of letters
```
split -d -l 5000 server.log log_
```
    Output: log_00, log_01, log_02...
- Prefix customization:    
```
split -l 1000 largefile chunk_
```
    Output: chunk_aa, chunk_ab...