The **uniq** command filters out repeated **adjacent** lines from a text stream. It is often paired with **sort** to get accurate results when duplicates are not already grouped.

---

## **Basic Duplicate Removal**

Example file: reading.txt

```
book
book
paper
paper
article
article
magazine
```

Command:

```
uniq reading.txt
```

Output:

```
book
paper
article
magazine
```

uniq removes consecutive repeated lines and keeps only the first occurrence from each group.

---

## **Counting Occurrences (-c)**

Use this when you want to know how many times each line appears.

Command:

```
uniq -c reading.txt
```

Output:

```
      2 book
      2 paper
      2 article
      1 magazine
```

The count appears on the left.

---

## **Showing Only Unique Lines (-u)**

Shows lines that appear _exactly once_ in the input.

Command:

```
uniq -u reading.txt
```

Output:

```
magazine
```

---

## **Showing Only Duplicate Lines (-d)**

Shows lines that appear more than once (but prints them once).

Command:

```
uniq -d reading.txt
```

Output:

```
book
paper
article
```

---

## **Importance of Sorting**

uniq only removes **adjacent** duplicates. If matching lines are separated, uniq will not detect them.

Example file:

```
book
paper
book
paper
article
magazine
article
```

Command:

```
uniq reading.txt
```

Output:

```
book
paper
book
paper
article
magazine
article
```

Nothing is removed because duplicates are not next to each other.

To fix this, sort the file first:

```
sort reading.txt | uniq
```

Output:

```
article
book
magazine
paper
```

Sorting groups identical lines together, allowing uniq to process them correctly. This pattern is widely used in shell scripting.

---

## **Common uniq + sort Patterns**

- Get unique lines (sorted):
```
sort file.txt | uniq
```
- Count and sort by frequency:
```
sort file.txt | uniq -c | sort -n
```
- View most common item:
```
sort file.txt | uniq -c | sort -nr | head
```