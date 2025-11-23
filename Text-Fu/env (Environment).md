### **What environment variables are**

- Environment variables store information that the shell and other programs use.    
- They describe your session, user details, system paths, and configuration.    
- You can read any variable by prefixing its name with `$`.    

Examples:

```
echo $HOME   # Shows your home directory
echo $USER   # Shows your username
```

---

## **The env Command**

### **What `env` does**

- The `env` command prints all environment variables currently active in your session.    
- Each line is a key-value pair.    

Example output:

```
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
```

You can use this to inspect how your environment is set up and debug configuration issues.

---

## **The PATH Variable**

### **What PATH is**

- PATH is one of the most important environment variables.    
- It contains a colon-separated list of directories.    

Example:

```
echo $PATH
```

### **Why PATH matters**

When you type a command:

1. The shell checks each directory listed in PATH.    
2. It looks for an executable with that name.    
3. It runs the first match it finds.    

If a program isn't in one of these directories, you’ll get:

```
command not found
```

### **Adding custom directories to PATH**

If you install a program in a non-standard location (like `/opt/coolapp/bin`), the shell won’t find it unless that directory is part of PATH.

You can fix this by updating PATH. For example:

```
export PATH="$PATH:/opt/coolapp/bin"
```

After this, you can run the program from anywhere without typing its full path.

---

## **Why environment variables matter**

- They customize your shell session.    
- They let you configure how programs behave.    
- They help you manage scripts, executables, and user-specific settings.    
- PATH, HOME, USER, SHELL, and PWD are some of the most commonly used variables.