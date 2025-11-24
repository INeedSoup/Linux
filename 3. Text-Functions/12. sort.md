The **sort** command arranges lines of text in a specific order. It works with plain text files and is commonly used when organizing lists, logs, or output from other commands.

---

## **Basic alphabetical sorting**

Example file:

file1.txt

```
dog
cow
cat
elephant
bird
```

Command:

```
sort file1.txt
```

Output:

```
bird
cat
cow
dog
elephant
```

The default behavior sorts lines in **ascending alphabetical order**.

---

## **Reverse alphabetical sorting**

Command:

```
sort -r file1.txt
```

Output:

```
elephant
dog
cow
cat
bird
```

The `-r` option reverses the default sorting order.

---

## **Numerical sorting**

If the file contains numbers or the comparison needs to be numeric, use the `-n` flag.

Command:

```
sort -n file1.txt
```

In your example, the content is text, so the order doesn't change. This option matters when the lines contain numbers like:

numbers.txt

```
10
2
100
50
```

Command:

```
sort -n numbers.txt
```

Output:

```
2
10
50
100
```

---

## **Additional useful options**

- `-k <field>`: Sort by a specific column or field
```
sort -k 2 file.txt
```
- `-t <delimiter>`: Use a custom delimiter (comma, colon, etc.)
```
sort -t "," -k 2 file.csv
```
- `-u`: Remove duplicate lines while sorting
```
sort -u file.txt
```
- `-h`: Human-readable sorting (works with sizes like 5K, 2M, 1G)
```
sort -h sizes.txt
```