### What `alias` Does

`alias` lets you create shortcuts for long or repetitive commands.  
It replaces a command or command sequence with a shorter name of your choice.

This helps you work faster and customize your shell to your style.

---

## Creating a Temporary Alias

Temporary aliases last only for the current session.

Example:

```
alias ll='ls -la'
```

Now typing `ll` runs:

```
ls -la
```

You can create shortcuts for anything:

```
alias update='sudo apt update && sudo apt upgrade'
alias gs='git status'
alias ..='cd ..'
```

---

## Making an Alias Permanent

To keep your aliases across terminal sessions, add them to your shell configuration file.

For Bash, the file is:

```
~/.bashrc
```

Steps:

1. Open the file:    
 ```
 nano ~/.bashrc
 ```    
2. Add your alias lines:
```
alias ll='ls -la'
alias update='sudo apt update && sudo apt upgrade'
```   
3. Save and exit.    
4. Reload the file or reopen the terminal:
```
source ~/.bashrc
```
    
Your aliases will now load automatically each session.

---
## Removing an Alias

To remove an alias from the current session:

```
unalias ll
```

If the alias was permanent, you must also delete it from `~/.bashrc` and reload the file:

```
source ~/.bashrc
```

---

## Extra Helpful Tips

### Show all current aliases

```
alias
```

### Prevent an alias from expanding (run the real command)

Prefix it with a backslash:

```
\ls
```

### Alias with multiple commands

Use quotes to wrap them:

```
alias cleanup='rm -i *.log && echo "Done"'
```

### Aliases do not take arguments

This is why many users switch to shell functions for advanced shortcuts.  
For example, functions let you do:

```
mkcd() { mkdir -p "$1" && cd "$1"; }
```