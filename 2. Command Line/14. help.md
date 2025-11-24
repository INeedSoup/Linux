### What `help` Does

The `help` command is built into the Bash shell.  
It shows information about **Bash built-in commands**, not external programs.

Built-ins are commands that Bash provides internally, such as:

- `cd`    
- `pwd`    
- `echo`    
- `history`    
- `alias`    
- `readonly`    

To get help for a built-in:

```
help echo
```

This prints:

- a description    
- syntax    
- options    
- usage notes    

It's the fastest way to learn about shell-specific features.

---

## Using `--help` for Programs

Most standard Linux commands are external programs and **not** Bash built-ins.  
For those, the `help` command will not work.

Instead, they provide their own help menu using the `--help` option.

Examples:

```
ls --help
cp --help
grep --help
tar --help
```

This displays:

- what the program does    
- how to use it    
- all available flags and arguments    

Most programs follow this convention, though not every single one.

---

## Extra Tips That Are Often Missed

### Check if a command is built-in or external

```
type cd
type ls
```

This tells you whether `help` or `--help` is appropriate.

### Use `help -d` to list all Bash built-ins

```
help -d
```

### Use the manual pages for deeper explanations

```
man ls
man bash
man find
```

Man pages give much more detail than `--help` or `help`.

### Quick keyword search in man pages

```
man -k copy
```

This finds all commands related to “copy”.

### For info-style documentation

Some tools use GNU info pages:

```
info coreutils
info ls
```

