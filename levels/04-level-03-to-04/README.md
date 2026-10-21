# Bandit Level 3 → Level 4

## Objective
Find and read a hidden file inside the `inhere` directory.

## Commands Used
Run in the remote bandit3 shell:
```bash
cd inhere
ls -la
```
Read the hidden file using its exact name from the listing:
```bash
# Replace HIDDEN_FILENAME with the actual filename, including its leading dots.
cat ./HIDDEN_FILENAME
```

## What I Learned
- `cd` changes the current directory.
- Filenames beginning with a dot are hidden from a normal `ls` listing.
- `ls -a` includes hidden entries; `-l` shows details such as permissions and size.
- `.` means the current directory and `..` means its parent; these are directory entries, not the target file.

## Status
- [x] Completed

## Notes
Use the filename actually listed rather than assuming a hidden filename from a walkthrough.
Use the discovered password to log into `bandit4` on port 2220.
No discovered passwords are included here.

## Reference
[Official Level 3 → 4 instructions](https://overthewire.org/wargames/bandit/bandit4.html)
