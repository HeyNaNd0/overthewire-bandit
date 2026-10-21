# Bandit Level 9 → Level 10

## Objective

Find a password hidden among human-readable strings inside a file containing binary data. The relevant text is identified by a specific character pattern.

## What I Learned

### 1. Identifying File Types

I learned that the `file` command examines a file's contents to determine its type.

Example:

`file example.dat`

Sometimes the output simply says `data`, meaning Linux cannot identify a more specific file format.

This does not necessarily mean the file is unreadable. It may contain binary data mixed with printable text.

### 2. Extracting Readable Text with strings

I discovered the `strings` command, which extracts sequences of printable characters from files.

Example:

`strings example.dat`

This is particularly useful when investigating binary files that contain readable information.

I learned that a file doesn't need to be a normal text file for Linux to extract useful text from it.

### 3. Combining strings and grep

I learned how to combine commands to extract information and then filter the results.

Example:

`strings example.dat | grep "ERROR"`

| Part | Purpose |
| --- | --- |
| `strings` | Extract printable character sequences |
| `example.dat` | File being inspected |
| `\|` | Pass output to another command |
| `grep` | Search for matching text |
| `"ERROR"` | Pattern to search for |

This technique is useful for troubleshooting and investigating unfamiliar files.

### 4. Discovering Commands Without Google

One of my biggest questions during this challenge was:

**How would I discover a command like `strings` if I had never used it before?**

I learned that Linux provides tools for discovering commands based on keywords.

For example:

`apropos printable`

This searches installed manual-page descriptions for the keyword `printable`.

Other examples:

- `apropos strings` searches for related manual entries.
- `man -k printable` performs a similar keyword search.
- `man strings` opens the command's manual.
- `strings --help` displays a usage summary if supported.
- `info strings` opens additional documentation if available.

I learned that `apropos` and `man -k` depend on the system's installed manual database, so they may not always return useful results.

### 5. Learning to Read Command Documentation

Instead of memorizing command syntax, I practiced a process for discovering and understanding unfamiliar Linux tools.

1. Read the problem carefully.
2. Identify important keywords.
3. Search for relevant commands using `apropos`.
4. Open the documentation using `man`.
5. Read the NAME, SYNOPSIS, DESCRIPTION, and OPTIONS sections.
6. Test the command.
7. Verify the results.

This gives me a repeatable way to approach unfamiliar Linux problems.

### 6. Understanding the Difference Between file, strings, and grep

| Command | Purpose |
| --- | --- |
| `file` | Identify a file's data type |
| `strings` | Extract readable character sequences |
| `grep` | Search text for a matching pattern |
| `apropos` | Discover commands through manual descriptions |
| `man` | Read documentation for a command |

Each command solves a different part of the problem.

### 7. Applying These Skills to Linux Administration

These techniques can be useful for:

- Investigating unknown files
- Troubleshooting applications
- Searching logs and command output
- Inspecting binary data
- Discovering unfamiliar Linux utilities
- Preparing for hands-on Linux administration exams such as LFCS

## My Biggest Takeaway

**I don't need to know every Linux command before encountering a problem. I need to know how to discover the right tool.**

This challenge taught me that Linux administration involves more than memorizing commands.

A good problem-solving approach is:

**Understand the problem → Discover the tool → Read the documentation → Test → Verify.**

Learning how to find answers directly in the terminal is a skill I want to continue developing.

## Skills Practiced

- `file`
- `strings`
- `grep`
- Linux pipes (`|`)
- `apropos`
- `man`
- `man -k`
- `--help`
- Searching Linux documentation
- Binary file inspection
- Command discovery and troubleshooting

## Challenge Status

Completed: Level 9 → Level 10

No passwords, sensitive information, or challenge-specific solutions are included.

## Credits

Challenge provided by [OverTheWire Bandit](https://overthewire.org/wargames/bandit/).
