# Linux Day 2: File and Directory Management

## Overview

Today I learned how to manage files and directories using Linux terminal commands. These commands are useful for everyday Linux administration and IT support tasks.

## Learning Objectives

- Create and manage directories.
- Create empty files.
- Copy and move files.
- Rename files and directories.
- Remove files and empty directories.
- Understand basic file management workflows.

## 1. Create a Directory — `mkdir`

The `mkdir` command is used to create a new directory.

```bash
mkdir practice
```

**Create multiple directories:**

```bash
mkdir documents backups scripts
```

**Create nested directories:**

```bash
mkdir -p projects/linux/day2
```

## 2. Create Files — `touch`

The `touch` command creates an empty file if it does not exist.

```bash
touch notes.txt
```

Create multiple files:

```bash
touch notes.txt backup.txt test.txt
```

## 3. Copy Files — `cp`

The `cp` command copies files from one location to another.

```bash
cp notes.txt backup.txt
```

Copy a file into another directory:

```bash
cp notes.txt backups/
```

## 4. Move and Rename Files — `mv`

The `mv` command moves files and directories or renames them.

**Rename a file:**

```bash
mv notes.txt linux-notes.txt
```

**Move a file:**

```bash
mv linux-notes.txt backups/
```

## 5. Remove Files — `rm`

The `rm` command removes files.

```bash
rm test.txt
```

**Important:** Use this command carefully because deleted files may not be easily recoverable.

Avoid using `rm -rf` unless you fully understand its effects.

## 6. Remove Empty Directories — `rmdir`

The `rmdir` command removes an empty directory.

```bash
rmdir old-folder
```

It will not remove a directory containing files.

## 7. Practical Lab

Let's practice these commands together.

```bash
mkdir linux-practice
cd linux-practice

mkdir documents backups
touch notes.txt

cp notes.txt backups/
mv notes.txt linux-notes.txt

ls -R
```

### Expected Directory Structure

```text
linux-practice/
├── backups/
│   └── notes.txt
├── documents/
└── linux-notes.txt
```

## 8. Useful Verification Commands

| Command | Purpose |
|---|---|
| `pwd` | Display current directory |
| `ls -l` | List files with details |
| `ls -R` | List directory contents recursively |
| `file notes.txt` | Identify file type |
| `stat notes.txt` | Display file metadata |

## 9. Key Takeaways

- `mkdir` creates directories.
- `touch` creates empty files.
- `cp` copies files.
- `mv` moves or renames files.
- `rm` removes files.
- `rmdir` removes empty directories.

## 10. Learning Progress

- [x] Learned basic file management commands.
- [x] Practiced creating files and directories.
- [x] Practiced copying and moving files.
- [ ] Practice independently in Kali Linux.

**Environment:** Kali Linux  
**Level:** Beginner  
**Status:** Practicing

---

*These are my personal learning notes based on hands-on Linux terminal practice. I am documenting my progress as I develop Linux administration and IT support skills.*
