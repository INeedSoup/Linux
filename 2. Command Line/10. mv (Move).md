### What `mv` Does

`mv` handles two major tasks:

1. **Renaming** files or directories    
2. **Moving** files or directories to a new location    

Unlike `cp`, `mv` does not create duplicates. It simply relocates or renames the original item.

---

## Renaming Files and Directories

To rename a file:

```
mv oldfile newfile
```

To rename a directory:

```
mv old_directory_name new_directory_name
```

This is one of the simplest and most common uses of `mv`.

---

## Moving Files and Directories

Move a file into a directory:

```
mv file2 /home/pete/Documents
```

Move multiple files:

```
mv file_1 file_2 /somedirectory
```

Using the `-t` option (target first), which is cleaner in complex moves:

```
mv -t /somedirectory file_1 file_2
```

### Moving directories

Unlike `cp`, `mv` does not require `-r`. It handles directories by default:

```
mv Projects/ /home/pete/Archive/
```

---

## Important Options

### Interactive mode (ask before overwriting)

```
mv -i source_file destination_directory
```

### Backup the old file before overwriting

Creates a backup with a tilde (~) at the end:

```
mv -b file1 directory_with_file1
```

### Verbose output (show what mv is doing)

```
mv -v file1 file2 /somedirectory
```

---

## Extra Helpful Tips

### Moving and renaming at the same time

```
mv notes.txt /home/pete/Documents/final_notes.txt
```

This both moves and renames the file in one command.

### Using wildcards

```
mv *.jpg /home/pete/Pictures
```

### Moving everything in a folder except specific files

```
mv !("important.txt") /backup
```

This requires extended globbing (`shopt -s extglob`).
