# Bandit Level 0 — SSH Login

## Objective
Connect to the Bandit server as `bandit0` using SSH.

## Commands Used
```bash
ssh -p 2220 bandit0@bandit.labs.overthewire.org
# After finishing a remote session:
exit
```

## What I Learned
- SSH opens a secure shell on a remote computer.
- `username@hostname` specifies the remote account and server.
- `-p 2220` selects Bandit's custom SSH port.
- Password input is not displayed while typing; press Enter to submit it.
- Commands entered after login run on the remote server. `exit` returns to the local shell.

## Status
- [x] Completed

## Notes
The initial SSH login is separate from the Level 0 → 1 file-reading challenge.
Keep discovered passwords in private local notes, outside published documentation.

## Reference
[Official Level 0 instructions](https://overthewire.org/wargames/bandit/bandit0.html)
