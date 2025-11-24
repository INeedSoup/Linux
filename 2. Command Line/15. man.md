### What `man` Does

`man` displays the manual pages for Linux commands and programs.  
These “man pages” are the built-in documentation available directly on your system.  
They are the most reliable source for:

- command descriptions    
- flags and options    
- examples    
- technical details    
- related commands    

If you're unsure how something works, the manual is usually the right place to look.

---

## Viewing a Manual Page

To open the manual for any command:

```
man ls
```

Inside a man page:

- Use the **arrow keys** to scroll    
- Use **Space** to jump one page down    
- Use **b** to go back one page    
- Press **q** to quit  

Man pages open in a viewer called `less`, so all its shortcuts work.

---

## Understanding Command Options with `man`

Man pages explain every flag for a command.  
For example, if you want to know what `-l` does in `ls -l`, the manual tells you clearly.

This makes `man` the best source for:

- understanding unfamiliar options    
- exploring advanced features    
- learning the precise behavior of a command    

---

## Extra Useful Features (Very Good to Know)

### Search inside a man page

Press `/` and type your search term:

```
/size
```

Press **n** for the next match.

### Jump to the start or end

- **g** → top    
- **G** → bottom    

### Find what section a manual page belongs to

```
man -f ls
```

This is the same as typing:

```
whatis ls
```

### Search for commands by keyword

```
man -k copy
```

This searches all man page descriptions for the word “copy”.

### Show a specific section

Sometimes a command has multiple man pages across different sections.  
For example:

```
man 5 passwd
```

opens the manual for the `passwd` file format, not the command.
