# Bandit Level 1 → Level 2

## Objective
Read the file named `-` in bandit1's home directory.

## Commands Used
Run in the remote bandit1 shell:
```bash
ls
cat ./-
```
Alternative using input redirection:
```bash
cat < -
```

## What I Learned
- A lone `-` has special meaning to many commands. `cat -` reads standard input instead of the file named `-`.
- `./` refers to the current directory, so `./-` unambiguously names the file.
- `<` makes the shell open a file and pass its contents to a command as standard input.
- Quoting `"-"` alone does not change how `cat` interprets that argument.

## Status
- [x] Completed

## Notes
Use the discovered password to log into `bandit2` on port 2220.
No discovered passwords are included here.

## Reference
[Official Level 1 → 2 instructions](https://overthewire.org/wargames/bandit/bandit2.html)
