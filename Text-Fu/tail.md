The `tail` command lets you view the end of a file. It’s especially useful for logs, where the most important information is often at the bottom.

---

## **Default Behavior**

### **Shows the last 10 lines**

```
tail /var/log/syslog
```

- Prints the final 10 lines of the file.    
- Helpful for checking recent log entries or file endings.    

---

## **Customizing the Line Count**

### **Use `-n` to specify how many lines to view**

```
tail -n 20 /var/log/syslog
```

- Displays the last 20 lines.    
- Works with any number you need.    

Example:

```
tail -n 5 file.txt
```

---

## **Real-Time Monitoring with `-f`**

### **Follow mode**

```
tail -f /var/log/syslog
```

- Shows the last lines, then keeps running.    
- Prints new lines as the file grows.    
- Perfect for watching active log files, debugging, or monitoring running services.    

This behavior makes `tail -f` a go-to command for system administrators and developers.

---

## **When tail is useful**

- Checking the latest log entries    
- Watching applications generate output    
- Debugging issues in real time    
- Inspecting file endings without opening the whole file