# Bandit Level 6 → Level 7

## Objective

Find a file somewhere on a Linux server that meets three requirements:

- Owned by a specific user
- Belongs to a specific group
- Has an exact file size

## What I Learned

### 1. Searching the Entire Linux Filesystem

Unlike previous levels, where I searched inside a specific directory, this challenge required searching the entire server.

I learned that `find /` starts searching at the root of the filesystem and recursively searches its directories.

### 2. Filtering Files by Ownership and Size

I learned how to combine multiple conditions using the `find` command.

| Option | Purpose |
| --- | --- |
| `-type f` | Search for regular files only |
| `-user` | Filter files by their owner |
| `-group` | Filter files by their group |
| `-size` | Filter files by their exact size when using the byte suffix `c` |

Combining these filters allows me to find files based on their metadata instead of knowing their names or locations.

### 3. Understanding Linux Permission Errors

While searching the entire filesystem, I encountered many `Permission denied` messages.

I learned that Linux restricts access to certain directories based on user permissions.

These errors are expected when searching directories I don't have permission to access.

### 4. Understanding Standard Input, Output, and Errors

One of the most important concepts I learned was that Linux commands use three standard streams.

| Number | Stream | Purpose |
| --- | --- | --- |
| `0` | stdin | Standard input |
| `1` | stdout | Normal command output |
| `2` | stderr | Error messages |

My biggest realization:

**0 goes IN. 1 and 2 come OUT.**

These numbers identify communication streams, not command success or failure.

### 5. Redirecting Error Messages

I learned that Linux allows command output to be redirected.

For example:

`2>/dev/null`

Breaking it down:

- `2` represents stderr.
- `>` redirects output.
- `/dev/null` discards anything written to it.

This allows me to hide unwanted error messages while keeping normal command results visible.

I also learned that redirecting errors doesn't fix permission problems. It only prevents those messages from appearing in the terminal.

### 6. Searching Efficiently

Instead of manually exploring directories, I can combine search filters and output redirection to find relevant files more efficiently.

This is useful for:

- Linux administration
- Troubleshooting
- Shell scripting
- Infrastructure engineering
- Automation

## My Biggest Takeaway

The most valuable lesson wasn't just finding a file. It was understanding how Linux handles command input, normal output, and errors.

I now understand why permission errors appear during filesystem searches and how to control which messages are displayed.

**Search precisely, understand the output, and filter unnecessary noise.**

## Skills Practiced

- Recursive filesystem searching
- File ownership and group filtering
- File size filtering
- Linux permissions
- Standard input (`stdin`)
- Standard output (`stdout`)
- Standard error (`stderr`)
- Shell output redirection
- `/dev/null`

## Challenge Status

Completed: Level 6 → Level 7

No passwords, exact target file paths, or challenge solutions are included.

## Credits

Challenge provided by [OverTheWire Bandit](https://overthewire.org/wargames/bandit/).
