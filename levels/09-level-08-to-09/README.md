# Bandit Level 8 → Level 9

## Objective

Find the only line in a text file that appears exactly once, while all other lines are repeated.

## What I Learned

### 1. Understanding the Problem Before Choosing Commands

I learned that I should first identify what the challenge is asking instead of trying every command provided.

For this challenge, I needed to:

- Identify repeated lines.
- Group identical lines together.
- Find the line that occurs only once.

This helped me narrow down the available commands to `sort` and `uniq`.

### 2. Using sort and uniq Together

The `sort` command arranges lines in order, placing identical lines next to each other.

The `uniq` command processes consecutive identical lines.

Example using a practice file:

`sort example.txt | uniq -u`

| Command | Purpose |
| --- | --- |
| `sort` | Sort lines so duplicates become adjacent |
| `\|` | Pass output from one command to another |
| `uniq` | Process consecutive identical lines |
| `-u` | Display only lines that occur once |
| `-c` | Count occurrences of adjacent identical lines |
| `-d` | Display lines that appear more than once |

**Important:** `uniq` does not detect duplicates scattered throughout a file unless identical lines are grouped together first.

### 3. Understanding Linux Pipes

I learned that the pipe operator (`|`) connects commands.

The output of the first command becomes the input of the second.

Example:

`sort example.txt | uniq -c`

This sorts the lines and then counts how many times each distinct line appears.

Pipes allow me to combine simple Linux commands to solve more complex problems.

### 4. Learning to Search Linux Manual Pages

One of my biggest discoveries was how to search inside `man` pages instead of reading the entire document.

Example:

`man uniq`

While inside the manual:

| Key | Action |
| --- | --- |
| `/word` | Search forward for a word |
| `?word` | Search backward |
| `n` | Move to the next match |
| `N` | Move to the previous match |
| `Space` | Move forward one page |
| `b` | Move backward one page |
| `g` | Go to the beginning |
| `G` | Go to the end |
| `q` | Exit the manual |

I learned that searching for words describing what I want to accomplish can help me discover command options.

For example, searching for `unique` inside the `uniq` manual helps locate the option that displays lines occurring only once.

### 5. Different Ways to Get Help in Linux

I learned that `man` pages aren't the only source of help available directly in the terminal.

| Command | Purpose |
| --- | --- |
| `man uniq` | Open the command's manual |
| `uniq --help` | Display a quick usage summary |
| `info uniq` | Open more detailed documentation, when available |
| `help cd` | Display help for a Bash built-in command |
| `apropos search` | Search manual descriptions for related commands |
| `tldr uniq` | Display practical examples if the separate `tldr` utility is installed |

Not every man page includes practical examples. Some focus primarily on syntax, descriptions, and available options.

I also learned that not every command supports `--help`, and not every system has all documentation utilities installed.

### 6. Developing Linux Problem-Solving Skills

Instead of memorizing hundreds of commands, I want to develop a repeatable troubleshooting process:

1. Understand the problem.
2. Identify what type of data I'm working with.
3. Determine which command performs the required operation.
4. Use documentation to discover the correct options.
5. Combine commands when necessary.
6. Verify that the result meets the requirements.

This approach will also help with my preparation for the Linux Foundation Certified System Administrator (LFCS) exam.

## My Biggest Takeaway

**Knowing how to find information is just as important as remembering commands.**

I don't need to memorize every Linux option. I need to understand what I'm trying to accomplish, know how to navigate documentation, and practice solving problems independently.

This challenge reinforced three important skills:

- Processing and filtering text.
- Combining commands using pipes.
- Finding answers through Linux documentation.

## Skills Practiced

- `sort`
- `uniq`
- `uniq -u`
- `uniq -c`
- `uniq -d`
- Linux pipes (`|`)
- Searching manual pages
- `man`, `info`, `--help`, `help`, and `apropos`
- Command discovery and troubleshooting

## Challenge Status

Level 8 → Level 9: Practiced and solution method identified.

No passwords or challenge-specific answers are included.

## Credits

Challenge provided by [OverTheWire Bandit](https://overthewire.org/wargames/bandit/).
