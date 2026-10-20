# OverTheWire Bandit - Learning Frictions

This document tracks concepts I struggled with, what confused me,
and what I learned while completing OverTheWire Bandit.

## Friction #001: Understanding SSH Accounts Between Levels

**Challenge:** Level 1 → Level 2
**Category:** SSH / Linux User Accounts
**Status:** Resolved

### What Confused Me

I didn't understand which machine or account I needed to SSH into
after completing each Bandit challenge.

I initially thought every level required connecting to a different server.

### What I Learned

All Bandit levels use the same SSH server, but each level uses
a different Linux user account.

| Challenge | SSH Account | Goal |
|---|---|---|
| Level 0 → 1 | bandit0 | Find password for bandit1 |
| Level 1 → 2 | bandit1 | Find password for bandit2 |
| Level 2 → 3 | bandit2 | Find password for bandit3 |

### Key Takeaway

For Level X → Level Y, SSH into banditX and find the password for banditY.

### Commands Learned

- `exit` - Close the current SSH session.
- `ssh bandit2@bandit.labs.overthewire.org -p 2220` - Connect as bandit2.
- `whoami` - Verify the current Linux account.

### Resolution

I now understand that moving between levels means authenticating
as a different Linux user on the same server, not connecting
to a different machine.

---

## Future Frictions

New challenges, mistakes, and lessons learned will be documented here
without publishing passwords, credentials, or challenge spoilers.
