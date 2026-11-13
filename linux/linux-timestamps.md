# Linux Timestamps

A timestamp is a record of the date and time when something happened.
Example: `2026-11-13 14:30:25`

## 3 Timestamps of a File

| Name | Meaning | Command |
|------|---------|---------|
| atime | Access time: when the file was last read | `ls -lu` |
| mtime | Modify time: when the file content last changed | `ls -l` (default) |
| ctime | Change time: when the file info (permission, name, owner) last changed | `ls -lc` |

Easy way to remember:
- **m** = modify
- **c** = change
- **u** = use (access)

## Useful Commands

```bash
date             # show current date and time
date +%Y-%m-%d   # show date in custom format
date +%s         # show Unix epoch time (seconds since 1 Jan 1970)
stat test.txt    # show atime, mtime, ctime of a file
touch test.txt   # create a file or update its timestamp
```

## Practice

```bash
echo "hello" > test.txt
ls -l test.txt
ls -lc test.txt
ls -lu test.txt

chmod 777 test.txt    # changes ctime only
ls -l test.txt        # mtime did not change
ls -lc test.txt       # ctime changed

echo "new line" >> test.txt   # changes mtime and ctime
```

## Note

Linux may not update atime every time a file is read. This is done to improve performance. It is normal.

## Why It Matters

- **System admin:** check which file changed and when, check old backups.
- **Logs:** files in `/var/log/` have a timestamp for every event.
- **Cybersecurity / forensics:** timestamps help find which files were changed after a break-in.
- **Automation:** backup scripts and cron jobs use time.
