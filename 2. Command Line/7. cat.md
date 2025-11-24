### What `cat` Does

`cat` stands for **concatenate**.  
It can display file contents, combine files, or create new files using redirection.

It's one of the simplest ways to read text files from the terminal.

---

## Viewing File Contents

To print the contents of a file to your terminal:

```
cat myfile.txt
```

This works well for small files.  
For long files, the output will scroll quickly, so tools like `less` or `more` are better.

---

## Concatenating Multiple Files

`cat` can display several files in sequence:

```
cat dogfile birdfile
```

The second file’s content appears immediately after the first.  
This is useful when merging or comparing small files.

---

## Creating Files with Output Redirection

`cat` can create a file using the redirection operator `>`:

```
cat > newfile.txt
```

You can type text directly in the terminal.  
Press **Ctrl+D** on a new line to save and exit.

### Important Warning

`cat > filename` **overwrites the file completely from the start**.  
It replaces everything, even if the file already existed.

If you want to add content without overwriting, use `>>`:

```
cat >> notes.txt
```

This appends text at the end of the file.

---

## Useful Options

### Number all lines:

```
cat -n file.txt
```

### Number only non-empty lines:

```
cat -b file.txt
```

---

## Related Command: `tac`

`cat` prints a file from top to bottom.  
`tac` does the opposite.

### Reverse output:

```
tac file.txt
```

This prints the last line first and the first line last.  
It’s handy when checking logs or when you want to see content in reverse order.

---

## Other Helpful Points

### Viewing a file with special characters visible

```
cat -v file.txt
```

### Squeezing repeated blank lines

```
cat -s file.txt
```

This reduces multiple empty lines to just one.

### Reading from standard input when no file is provided

If you run:

```
cat
```

and press Enter, `cat` waits for you to type.  
Press **Ctrl+D** to end the input.
