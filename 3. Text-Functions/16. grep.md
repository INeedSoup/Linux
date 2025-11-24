The **grep** command searches for text patterns in files or streams. It is one of the most frequently used tools in Linux because it helps you quickly locate information without manually scanning large outputs.

---

## **Basic Usage**

To find all lines in a file containing a given word:

```
grep fox sample.txt
```

This prints every line in **sample.txt** that contains “fox”.

grep can search:

- single files    
- multiple files    
- command output via pipes    
- entire directories (with recursive options)    

---

## **Pattern Matching with -e**

The `-e` option tells grep that the next argument is a pattern. This is helpful when the pattern begins with a hyphen.

Example:

```
grep -e "-v" file.conf
```

Without `-e`, grep would treat `-v` as the “invert match” option instead of the text you are trying to search for.

You can also supply multiple patterns using repeated `-e` options:

```
grep -e error -e warning logfile
```

---

## **Useful grep Options**

### **Case-insensitive search (-i)**

```
grep -i pattern file.txt
```

Matches regardless of letter case.

### **Count matching lines (-c)**

```
grep -c fox sample.txt
```

Outputs the number of lines that contain the pattern.

### **Show only the matched text (-o)**

```
grep -o fox sample.txt
```

Displays only the exact portions that match.

### **Use a file of patterns (-f)**

```
grep -f patterns.txt sample.txt
```

Searches using every pattern listed in patterns.txt.

### **Recursive search (-r or -R)**

```
grep -r TODO /project
```

Searches all files in a directory tree.

### **Invert match (-v)**

```
grep -v error logfile
```

Shows all lines that _do not_ match the pattern.

### **Show line numbers (-n)**

```
grep -n fox sample.txt
```

---

## **Regular Expression Examples**

grep supports regular expressions, giving you powerful matching features.

- Find lines ending with .txt    
```
grep '.txt$' filenames.txt
```
- Find lines starting with a number
```
grep '^[0-9]' data.txt
```
- Match any of several words
```
grep -E 'cat|dog|bird' animals.txt
```

(Use `grep -E` for extended regex.)

---

## **Using grep with Other Commands**

grep becomes even more powerful when used in pipelines.

- Filter environment variables
```
env | grep -i user
```
- Find active processes containing “ssh”
```
ps aux | grep ssh
```
- Search inside a directory listing
```
ls /somedir | grep '.txt$'
```
