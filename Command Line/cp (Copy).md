### What `cp` Does

`cp` copies files or directories from one location to another.  
The basic syntax is:

```
cp [SOURCE] [DESTINATION]
```

You can copy files, rename them during the copy, or duplicate entire directory structures.

---

## Basic File Copying

To copy a file into a directory:

```
cp mycoolfile /home/pete/Documents/cooldocs
```

To copy a file and give it a new name:

```
cp mycoolfile /home/pete/Documents/mycoolfile_backup
cp oldname newname
```

---

## Using Wildcards for Bulk Copying

Wildcards help you match multiple files in one go.

- `*` matches any number of characters    
- `?` matches a single character    
- `[]` matches any one character in the brackets    

Example: copy all JPEG images:

```
cp *.jpg /home/pete/Pictures
```

This is very useful for copying batches of related files.

---

## Copying Directories (Recursive Copy)

You must use the recursive option to copy folders:

```
cp -r Pumpkin/ /home/pete/Documents
```

This duplicates the directory along with all subfolders and files.

---

## Handling Overwrites

### Prevent accidental overwriting

```
cp -i mycoolfile /home/pete/Pictures
```

The `-i` option asks for confirmation before replacing an existing file.

### Force overwrite without prompts

```
cp -f mycoolfile /home/pete/Pictures
```

This is useful in scripts or automation where no user input is expected.

---

## Preserving File Attributes

Normally, copied files take on new timestamps and may change ownership.

To keep the original timestamps, permissions, and ownership:

```
cp -p mycoolfile /home/pete/backups/
```

This is helpful for backups, migrations, and any situation where file metadata matters.

---

## Other Helpful `cp` Tips

### Copy multiple files at once

```
cp file1 file2 file3 /home/pete/Documents
```

### See what is being copied (verbose mode)

```
cp -v mycoolfile /home/pete/Documents
```

### Combine flags

```
cp -rvp source/ destination/
```

This copies a directory recursively, preserves attributes, and shows progress.
