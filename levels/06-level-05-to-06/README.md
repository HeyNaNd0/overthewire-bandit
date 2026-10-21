# Bandit Level 5 → Level 6

## Status

- [x] Completed

## Objective

Find a file somewhere inside a directory structure that meets three requirements:

- Human-readable
- Exactly 1,033 bytes
- Not executable

## What I Learned

### 1. Searching directories recursively

I learned that the `find` command can search through an entire directory structure, including nested subdirectories.

This is much more efficient than manually opening every folder and inspecting individual files.

### 2. Filtering files by properties

The `find` command supports filters that narrow down search results.

| Option | Purpose |
| --- | --- |
| `-type f` | Search only for regular files |
| `-size 1033c` | Match files exactly 1,033 bytes |
| `!` | Negate a condition |
| `-executable` | Check whether the current user can execute a file |

Combining these filters makes searching faster and more precise.

### 3. Understanding file types

I learned that the `file` command examines file contents to identify their type.

For example, a file might be reported as:

- ASCII text
- Binary data
- Executable
- Compressed data

This is useful because file extensions and filenames do not always tell you what a file actually contains.

### 4. Understanding hidden files

Linux filenames beginning with a dot (`.`) are hidden from normal directory listings.

Hidden files are not necessarily protected or encrypted. They are simply omitted from standard listings unless explicitly requested.

### 5. Absolute paths vs. relative paths

An absolute path starts at the filesystem root (`/`) and identifies a file's location regardless of the current working directory.

A relative path identifies a location based on the current working directory.

Understanding both makes navigating Linux filesystems easier.

## My Biggest Takeaway

I don't need to manually inspect hundreds of files.

Instead, I can combine Linux commands and filters to narrow a large search down to a small number of candidates.

**The key lesson: Search intelligently instead of searching manually.**

## Skills Practiced

- Linux filesystem navigation
- Recursive file searching
- File size filtering
- File permission checks
- File type identification
- Hidden files
- Absolute and relative paths
