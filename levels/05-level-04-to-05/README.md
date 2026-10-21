# Bandit Level 4 → Level 5

## Objective
Find the only human-readable file in the `inhere` directory and read it.

## Commands Used
Run in the remote bandit4 shell:
```bash
cd inhere
ls
file ./*
```
Look for the file identified as text, then read that exact path:
```bash
# Replace TEXT_FILENAME with the filename identified by file.
cat ./TEXT_FILENAME
```
If displaying binary data leaves the terminal unreadable:
```bash
reset
```

## What I Learned
- `file` inspects file contents to identify their type; the filename alone may not tell us what a file contains.
- `./*` expands to the non-hidden entries in the current directory, with a safe `./` prefix for names beginning with dashes.
- Inspect file types before using `cat`; binary data can display unreadable characters or affect terminal output.
- `reset` can restore a terminal affected by displaying binary data.

## Status
- [x] Completed

## Notes
Use the discovered password to log into `bandit5` on port 2220.
Next challenge: [Level 5 → 6](../06-level-05-to-06/README.md).
No discovered passwords are included here.

## Reference
[Official Level 4 → 5 instructions](https://overthewire.org/wargames/bandit/bandit5.html)
