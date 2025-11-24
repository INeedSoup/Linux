### What `cd` Does

`cd` moves you to a different directory in the filesystem.  
It’s one of the core commands for navigating the terminal.

---

## Understanding Paths

### Absolute Path

- Starts from the root directory `/`.
    
- Always begins with `/`.
    
- Works no matter where you currently are in the filesystem.
    
- Example:
    
    `/home/pete/Desktop`
    

### Relative Path

- Based on your current location.
    
- Does not start with `/`.
    
- Useful for moving into nearby folders without typing full paths.
    
- Example:  
    If you're in `/home/pete/Documents` and want to enter `taxes`:
    
    `cd taxes`
    

---

## Basic Usage of `cd`

### Using an Absolute Path

Takes you directly to the target directory:

`cd /home/pete/Pictures`

### Using a Relative Path

Used when you're already in the parent directory:

`cd Hawaii`

This only works if Hawaii is inside your current directory.

---

## Helpful Navigation Shortcuts

### `.`

Represents the current directory.

`cd .`

(Usually does nothing, but useful in scripts.)

### `..`

Moves you to the parent directory.

`cd ..`

### `~`

Takes you to your home directory.

`cd ~`

### `-`

Switches back to the previous directory, like an undo for navigation.

`cd -`

---

If you want, I can also put together a quick practice worksheet with questions based on