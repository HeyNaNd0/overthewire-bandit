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

## Friction #002: Repeated SSH Logins Between Lessons

**Challenge:** Moving between Bandit levels
**Category:** SSH / Learning Workflow
**Status:** Open question

### What Feels Frustrating

Having to close an SSH session and authenticate with a different account for each lesson feels repetitive and interrupts my learning momentum. I would prefer a workflow that lets me progress through the lessons within one continuous session.

### What I Understand

The levels already run on the same server. The repeated logins involve switching Linux user accounts rather than connecting to a new device or node.

### Question to Explore

Why does each level require a separate user account and SSH login? What learning or access-control benefits does this structure provide compared with completing all lessons under one account in a continuous session?

---

## Future Frictions

New challenges, mistakes, and lessons learned will be documented here
without publishing passwords, credentials, or challenge spoilers.
