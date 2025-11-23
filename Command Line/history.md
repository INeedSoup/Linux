### What `history` Does

The shell keeps a list of all the commands you’ve run.  
The `history` command shows that list so you can review or reuse past commands without retyping them.

---

## Viewing Command History

To view your entire command list:

```
history
```

Each entry is numbered.  
Those numbers are useful for deleting specific entries or re-running commands.

---

## Re-running Previous Commands

### Up Arrow

Scroll backward through your command list one step at a time.

### `!!`

Runs the last command again.  
Example:

```
cat file1
!!
```

### `!<number>`

Runs a specific command from the history list:

```
!42
```

This re-runs command number 42.

---

## Searching Your History

### Reverse Search (Ctrl+R)

Press `Ctrl+R` and start typing part of a command.  
The shell shows the newest matching command.

Press `Ctrl+R` again to move to an older match.  
Press Enter to execute the displayed command.

This is one of the fastest ways to find long or complex commands you used earlier.

---

## Managing Your History

### Clear the in-memory history:

```
history -c
```

### Save the current session’s history to the history file:

```
history -w
```

This is useful before closing a terminal session, especially in temporary shells.

### Delete a specific entry:

```
history -d <number>
```

Example:

```
history -d 101
```

This removes the entry numbered 101.

---

## Other Helpful Terminal Tools

### Clear the terminal screen

```
clear
```

This doesn’t delete anything. It just cleans up your view.

### Tab Completion

Press Tab after typing the beginning of a command, file, or directory name.  
The shell auto-completes it when possible.

If there are multiple matches, pressing Tab twice shows all possible options.

Tab completion saves time and avoids typos, especially with long paths or filenames.

