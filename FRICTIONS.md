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

## Friction #003: Finding Practical Examples in Manual Pages

**Challenge:** Learning unfamiliar commands during Levels 8 → 9 and 9 → 10
**Category:** Linux Documentation / Command Discovery
**Status:** Ongoing

### What Feels Frustrating

Searching manual pages is not always straightforward, especially when I don't yet know the terminology used to describe an option. Finding a relevant description can take considerable effort, and understanding the syntax does not always make it clear how to apply the command.

The `uniq` manual page I consulted did not include practical usage examples. This made it harder to connect the documented options with the task I wanted to accomplish.

### What I Would Like to See

In 2026, I would expect terminal documentation to make information easier to discover through clearer explanations, more detailed guidance, and interactive search or navigation.

I would like every manual page to include a consistent examples section with complete commands and a plain-language explanation of what each command does. The command-and-explanation format I have seen in `kubectl` help is the kind of approach I find useful.

Examples should cover common tasks, explain the options used, and show expected results where practical. This would help learners move from reading a reference to using a command with confidence.

### Question to Explore

How can Linux documentation preserve its technical detail while making practical examples and relevant information easier for new users to find?

---

## Future Frictions

New challenges, mistakes, and lessons learned will be documented here
without publishing passwords, credentials, or challenge spoilers.
