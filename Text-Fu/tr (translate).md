The **tr** command translates, deletes, or squeezes characters from standard input. It works well in pipelines and is often used for quick text cleanup or transformation.

---

## **Basic Character Translation**

You can replace one set of characters with another. This is commonly used to change case.

Example:

```
echo "hello world" | tr a-z A-Z
```

Output:

```
HELLO WORLD
```

- The first set (`a-z`) is mapped to the second set (`A-Z`).    
- tr works only on characters, not whole words or patterns.    

---

## **Deleting Characters (-d)**

Use the `-d` option to remove specific characters from the input.

Example:

```
echo "My address is 123 Main Street" | tr -d '0-9'
```

Output:

```
My address is  Main Street
```

Here, every digit between 0 and 9 is removed.

This is commonly used for:

- removing digits    
- removing punctuation    
- stripping unwanted symbols    

---

## **Squeezing Repeated Characters (-s)**

The `-s` option replaces repeated characters with a single instance.

Example:

```
echo "Hello      World,   how   are   you?" | tr -s ' '
```

Output:

```
Hello World, how are you?
```

This is helpful when cleaning up:

- extra spaces    
- repeated punctuation    
- long sequences of the same character    

---

## **Other helpful uses**

- Replace tabs with spaces:
```
tr '\t' ' ' < file.txt
```
- Keep only certain characters by combining with complement:
```
tr -cd 'a-zA-Z\n' < file.txt
```
    This deletes everything except letters and newlines.
- Convert multiple characters at once:
```
echo "abc123" | tr 'a1c' 'XYZ'
```
Output:
```
    XbZ23
```

