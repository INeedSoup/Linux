### Filenames in Linux

Linux does not rely on file extensions to determine what type of data a file contains.  
A file called `banana.jpeg` might not be a picture at all, and `funny.gif` could just be an empty text file.  
Extensions are optional and mostly for human convenience.

Because of this, filenames don’t always tell you the true format or purpose of a file.

---

## What the `file` Command Does

The `file` command inspects the actual contents of a file, not its name.  
It analyzes the data inside and prints a description of what type of file it really is.

This makes it reliable when you’re unsure about a file’s origin or its correct format.

---

## Basic Usage

To identify a file’s type, run:

```
file banana.jpg
```

The output might be something like:

```
banana.jpg: JPEG image data
```

Or, if the file isn’t actually a picture:

```
banana.jpg: ASCII text
```

The command works the same way with any file type.

