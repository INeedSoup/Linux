### What `find` Does

`find` searches for files or directories starting from a given path and looks through all subdirectories automatically.  
It’s one of the most powerful search tools in Linux.

Basic syntax:

```
find [path] [expression]
```

---

## Searching by Name

To search for a file named `puppies.jpg` inside `/home`:

```
find /home -name puppies.jpg
```

This checks `/home` and every folder inside it.

### Case-insensitive search

```
find /home -iname puppies.jpg
```

This matches `puppies.jpg`, `PUPPIES.JPG`, or any variation.

---

## Searching by Type

Use `-type` to limit what you're searching for:

- `-type f` → regular files    
- `-type d` → directories    

Example: find a directory named `MyFolder`:

```
find /home -type d -name MyFolder
```

Example: find all `.txt` files:

```
find /home -type f -name "*.txt"
```

---

## Recursive Searching (Built-in)

There is no special flag needed.  
`find` automatically searches:

- the directory you specify    
- all subdirectories    
- and their subdirectories    

That’s what makes `find` so powerful.

---

## Additional Useful Features (Important Extras)

### Search by size

```
find /var/log -size +10M
```

Finds files larger than 10 MB.

### Search by modification time

```
find /home -mtime -1
```

Finds files modified in the last day.

### Search and delete (dangerous, use with caution)

```
find /tmp -type f -name "*.log" -delete
```

### Search and run a command on every match

```
find . -type f -name "*.txt" -exec cat {} \;
```

Prints every `.txt` file in the current directory tree.

### Search for empty files or directories

```
find . -empty
```

---

## A safer search using `-print`

To ensure you only display the results:

```
find /home -type f -name "*.jpg" -print
```
