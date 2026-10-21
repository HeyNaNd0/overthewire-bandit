# Bandit Level 7 → Level 8

## Objective

Find a specific word inside a text file and identify the information associated with it.

## What I Learned

### 1. Searching Inside Files with grep

I learned that `grep` searches the contents of files, not just filenames.

This is useful when working with large text files, application logs, and configuration files.

Example:

`grep "ERROR" application.log`

This displays lines containing the word ERROR.

### 2. Understanding grep Options

| Option | Purpose |
| --- | --- |
| `-i` | Search without case sensitivity |
| `-n` | Display matching line numbers |
| `-v` | Display lines that do not match |
| `-r` | Search recursively through directories |

### 3. Combining Linux Commands with Pipes

I learned that the pipe operator (`|`) passes the output of one command to another.

Example:

`sort application.log | uniq -c`

- `sort` groups identical lines together.
- `uniq` processes adjacent duplicate lines.
- `-c` counts how many times each line occurs.

I also learned that `uniq` alone does not count duplicates scattered throughout a file. Sorting first solves that problem.

### 4. Alternative Ways to Search Text

Although `grep` was sufficient for this challenge, I explored other approaches:

| Command | Purpose |
| --- | --- |
| `strings` | Extract readable text from files, including binary data |
| `sort` | Sort lines alphabetically |
| `uniq` | Remove adjacent duplicate lines |
| `tr` | Translate or remove characters |
| `xxd` | Display file contents in hexadecimal |
| `man` | Read command documentation |

I learned that combining commands can be powerful, but the simplest solution is often the best.

### 5. Understanding Other Linux Utilities

The challenge also introduced several commands that will be useful in later exercises.

| Command | Purpose |
| --- | --- |
| `base64` | Encode and decode data using Base64 |
