### What `whatis` Does

`whatis` gives you a **one-line summary** of a command, taken from the _NAME_ section of its manual page.  
It’s a quick way to remind yourself what a command does without opening the full `man` page.

Think of it like a dictionary lookup for Linux commands.

---

## Basic Usage

To see what a command is for:

```
whatis cat
```

Example output:

```
cat (1) – concatenate files and print on the standard output
```

This short description is pulled directly from the command’s man page.

---

## Handling Multiple Manual Sections

Some commands appear in more than one manual section.  
If so, `whatis` will show an entry for each version.

For example:

```
whatis passwd
```

You might see:

```
passwd (1) – change user password
passwd (5) – password file format
```

This helps you understand that the same keyword refers to different things depending on the context.

---

## Extra Helpful Tips

### Update the `whatis` database (if entries look missing)

Some systems need the database refreshed:

```
sudo mandb
```

### Search for a command by keyword (`apropos`)

If you don't remember the exact command name but know what it relates to:

```
apropos network
```

This lists all commands whose descriptions mention “network”.

### Check the man section used

The number in parentheses tells you the manual section:

- **1** = user commands    
- **5** = file formats    
- **8** = system admin commands    