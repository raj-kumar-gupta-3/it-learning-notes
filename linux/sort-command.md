# Sort Command in Linux

## Introduction

The `sort` command is used to arrange lines of text in a file.

It can sort text alphabetically and numbers in different orders.

## 1. Basic Sort

The `sort` command arranges text in alphabetical order.

Example:

```bash
sort names.txt
```

This displays the names in alphabetical order.

## 2. Create a Practice File

```bash
nano names.txt
```

Write:

```text
Raj
Amit
Suman
Bikash
```

Save the file and run:

```bash
sort names.txt
```

## 3. Reverse Sort (-r)

The `-r` option sorts lines in reverse alphabetical order.

```bash
sort -r names.txt
```

## 4. Numeric Sort (-n)

The `-n` option sorts numbers by their numeric values.

```bash
sort -n numbers.txt
```

Example file:

```text
50
10
100
20
```

Result:

```text
10
20
50
100
```

## 5. Reverse Numeric Sort

We can use `-nr` to sort numbers from largest to smallest.

```bash
sort -nr numbers.txt
```

## 6. Save Sorted Output

We can use `>` to save sorted results in another file.

```bash
sort names.txt > sorted.txt
```

To see the result:

```bash
cat sorted.txt
```

## 7. Sort and Remove Duplicate Lines (-u)

The `-u` option sorts lines and removes duplicate lines.

```bash
sort -u names.txt
```

## 8. Check Sort Order (-c)

The `-c` option checks whether a file is already sorted.

```bash
sort -c names.txt
```

## Important Points

- `sort` sorts lines alphabetically.
- `sort -r` sorts in reverse order.
- `sort -n` sorts numbers correctly.
- `sort -nr` sorts numbers from largest to smallest.
- `sort -u` removes duplicate lines.
- `sort -c` checks the sorting order.
- `sort file.txt > output.txt` saves sorted results.

## Practice

I practiced the Linux sort command using text files and different sorting options.
