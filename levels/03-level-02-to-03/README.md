# Bandit Level 2 → Level 3

## Objective
Read the file whose name contains spaces in bandit2's home directory.

## Commands Used
Run in the remote bandit2 shell:
```bash
ls
cat "./--spaces in this filename--"
```
For the older filename without leading or trailing dashes:
```bash
cat "./spaces in this filename"
```

## What I Learned
- The shell normally splits unquoted spaces into separate arguments.
- Quotes keep a filename containing spaces together as one argument.
- Prefixing a filename with `./` also prevents leading dashes from being treated as command options.
- Tab completion helps enter filenames accurately. Use the exact name shown by `ls`.

## Status
- [x] Completed

## Notes
The current official instructions name the file `--spaces in this filename--`; older versions used `spaces in this filename`.
Use the discovered password to log into `bandit3` on port 2220.
No discovered passwords are included here.

## Reference
[Official Level 2 → 3 instructions](https://overthewire.org/wargames/bandit/bandit3.html)
