### What `mkdir` Does

`mkdir` creates new directories (folders) in the filesystem.  
You can create one directory, many directories, or entire nested paths in a single command.

---

## Creating a Single Directory

To make a directory in your current location:

```
mkdir documents
```

If the folder doesn’t exist, it will be created. If it already exists, you’ll get an error unless you use the `-p` option.

---

## Creating Multiple Directories

You can create several directories at once:

```
mkdir books paintings
```

This is an easy way to prepare multiple project or category folders.

---

## Creating Nested Directories (Parent Option)

To create deeper directory structures in one command, use:

```
mkdir -p books/hemmingway/favorites

mkdir -p home/{employee,manager}/{name,address,contact}

```

The `-p` option does two things:

1. Creates any missing parent directories    
2. Prevents errors if parts of the path already exist    

This is very useful for scripting or building structured folder layouts.

---

## Extra Helpful Tips

### Create a directory in another location

```
mkdir /home/pete/projects
```

### See a message for each directory created (verbose)

```
mkdir -v books poetry drama
```

### Combine flags

```
mkdir -vp projects/python/scripts
```

This shows output while also creating all parent directories.

