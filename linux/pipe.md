# Linux Pipe (|)

Pipe is used to connect two commands in Linux. It takes the output of the first command and sends it to the second command.

For example, when we use `lscpu`, it shows all CPU information. But sometimes we only need the CPU model name. We can use pipe with grep to find it.

### Syntax

```bash
command1 | command2
```

### Examples

**1. Show CPU information**

```bash
lscpu | grep CPU
```

This command shows only the lines that contain the word CPU.

**2. Show RAM information**

```bash
free -h | grep Mem
```

This command shows the RAM information.

**3. Count files**

```bash
ls | wc -l
```

This command counts the lines in the output of ls.

**4. Search a running process**

```bash
ps aux | grep firefox
```

This command searches for Firefox in the running process list.

**5. Show IP address information**

```bash
ip addr | grep inet
```

This command shows lines that contain IP address information.

**6. Sort names**

```bash
cat names.txt | sort
```

This command sorts the names in alphabetical order.

**7. Remove duplicate lines**

```bash
sort names.txt | uniq
```

This command sorts the names and removes duplicate lines.

**8. Show first 5 lines**

```bash
ls | head -5
```

This command shows the first five lines of the output.

**9. Show last 5 lines**

```bash
ls | tail -5
```

This command shows the last five lines of the output.

**10. Save CPU information**

```bash
lscpu | tee cpu.txt
```

This command displays CPU information and also saves it in a file named `cpu.txt`.

### Using Multiple Pipes

We can also use more than one pipe in a single command.

```bash
cat names.txt | sort | uniq
```

First, it reads the file. Then it sorts the names and removes duplicate lines.

```bash
ps aux | grep firefox | wc -l
```

This command searches for Firefox-related lines and counts them.

### Where do we use Pipe?

We use pipe when we want to filter command output, search for specific information, count results or pass data from one command to another.

It is useful in Linux system administration, troubleshooting and daily terminal work.

### Practice

1. Use `lscpu` with grep to find CPU information.
2. Use `free -h` with grep to find RAM information.
3. Count the files in your current directory.
4. Search for Firefox processes.
5. Sort the names in a text file.
6. Find and remove duplicate lines.
7. Display the first five lines of a command output.
8. Save CPU information into a file.
