# Bandit Level 0 → Level 1

## Objective
Read the `readme` file in bandit0's home directory to obtain the password for bandit1.

## Commands Used
Run in the remote bandit0 shell:
```bash
pwd
ls
cat readme
exit
```
Then connect from the local terminal and enter the password found in `readme`:
```bash
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

## What I Learned
- `pwd` prints the current directory.
- `ls` lists visible files and directories.
- `cat` displays a text file's contents.
- Each next level uses a new account and the password discovered in the previous challenge.

## Status
- [x] Completed

## Notes
Save the solution method as well as the password: Bandit passwords can change.
No discovered passwords are included here.

## Reference
[Official Level 0 → 1 instructions](https://overthewire.org/wargames/bandit/bandit1.html)
