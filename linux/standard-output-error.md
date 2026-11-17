
# Standard Output and Standard Error in Linux

## Introduction

When we run a command in Linux, it can show normal results or error messages.

Linux has three standard streams:

- stdin: Takes input.
- stdout: Shows normal output.
- stderr: Shows error messages.

## 1. Standard Input (stdin)

Standard Input is used to give data to a command.

Example:

```bash
cat
```

Type some text and press Enter.

Press Ctrl + D to finish.

## 2. Standard Output (stdout)

Standard Output shows the normal result of a command.

Example:

```bash
echo "Hello Linux"
```

Output:

```text
Hello Linux
```

Another example:

```bash
ls
```

This command shows files and folders.

## 3. Standard Error (stderr)

Standard Error shows an error message when a command has a problem.

Example:

```bash
ls wrong-folder
```

It shows an error because the folder does not exist.

## 4. Save Normal Output

We can use `>` to save normal output in a file.

```bash
echo "Learning Linux" > output.txt
```

To read the file:

```bash
cat output.txt
```

## 5. Save Error Messages

We can use `2>` to save error messages in a file.

```bash
ls wrong-folder 2> error.txt
```

To read the error:

```bash
cat error.txt
```

## 6. Add Output to a File

We can use `>>` to add new text without deleting old text.

```bash
echo "First line" >> output.txt
echo "Second line" >> output.txt
```

## 7. Save Output and Errors Separately

```bash
ls Documents wrong-folder > output.txt 2> error.txt
```

- `output.txt` saves normal output.
- `error.txt` saves error messages.

## 8. Save Output and Errors in One File

```bash
ls Documents wrong-folder > result.txt 2>&1
```

This saves both normal output and error messages in one file.

## Important Points

- `stdin` means input.
- `stdout` means normal output.
- `stderr` means error output.
- `>` saves normal output.
- `>>` adds new text to a file.
- `2>` saves error messages.
- `2>&1` sends errors to the same place as normal output.

## Practice

I practiced standard input, standard output, standard error, and output redirection using Linux terminal commands.
