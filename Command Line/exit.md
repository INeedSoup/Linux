### What `exit` Does

The `exit` command ends your current shell session.  
When you type:

```
exit
```

the shell process stops, and you are returned to:

- the parent shell    
- the terminal emulator    
- or the login screen (if it was a login shell)    

It works in nearly every shell environment.

---

## The `logout` Command

`logout` also ends a session, but it is designed specifically for **login shells**.

Example:

```
logout
```

On many modern systems, `exit` and `logout` behave the same.  
However, `logout` won’t work inside a subshell or a non-login shell, while `exit` always works.

---

## Closing the Terminal Window

If you're using a graphical terminal, simply closing the window also ends the shell session.  
The window manager sends a signal that terminates the running shell.

This is the fastest way to exit when you're done and don’t need to run a final command.

---

## Extra Helpful Notes

### Exit with a status code

Every command returns a status number. You can choose the status when exiting:

```
exit 0     # success
exit 1     # general error
```

### Exiting a subshell

If you started a secondary shell (like running `bash` inside a shell), `exit` leaves only that subshell and returns you to the previous one.

### Exiting a script

In shell scripts, `exit` ends the script immediately:

```
exit 1
```
