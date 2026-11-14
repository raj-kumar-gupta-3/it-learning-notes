# Linux File and Folder Commands

Basic commands to copy, move, rename and remove files and folders.

## Setup for Practice

```bash
mkdir practice
cd practice
touch a.txt
mkdir myfolder
```

- `mkdir` creates a folder
- `touch` creates an empty file
- `cd` goes inside a folder

## 1. Copy (`cp`)

Makes a duplicate. The original stays.

```bash
cp a.txt b.txt          # copy a.txt as b.txt
cp a.txt myfolder/      # copy a.txt into myfolder
cp -r myfolder backup   # copy a folder (-r is needed)
```

`-r` means recursive: the folder and everything inside it.

## 2. Move (`mv`)

Moves a file from one place to another. The original is removed from the old place.

```bash
mv b.txt myfolder/      # move b.txt into myfolder
mv myfolder/b.txt .     # move it back to the current folder (.)
```

## 3. Rename (`mv`)

Linux has no separate rename command. `mv` also changes the name.

```bash
mv a.txt new.txt        # rename a.txt to new.txt
mv myfolder photos      # rename folder to photos
```

## 4. Remove (`rm`)

```bash
rm new.txt              # delete a file
rm -r photos            # delete a folder and everything inside
rmdir backup            # delete an empty folder only
rm -i new.txt           # ask before deleting
```

## Warning

- Files deleted with `rm` do not go to a Recycle Bin. They cannot be recovered easily.
- Think twice before using `rm -r`.
- Never run `rm -rf /`. It can delete the whole system.

## Summary

| Task | Command |
|------|---------|
| Copy | `cp` |
| Move | `mv` |
| Rename | `mv` |
| Remove | `rm` |  ye sb kaha type kare
