# Bandit Level 10 → Level 11

## Objective

Learn how to decode Base64-encoded data stored in a file using Linux command-line tools.

**Challenge:** [OverTheWire Bandit](https://overthewire.org/wargames/bandit/)

## 1. What Is Base64?

Base64 is a method of encoding binary data into printable text characters.

It is commonly used to represent data in configuration files, APIs, certificates, and other systems.

**Important:** Base64 is encoding, not encryption. It does not protect sensitive information.

Example:

| Original text | Base64 encoded |
| --- | --- |
| `hello` | `aGVsbG8=` |

Encoding transforms data into a different representation. Decoding reverses that transformation.

## 2. Discovering the Base64 Command

The challenge mentioned Base64, but I needed to learn how to use the Linux command.

I opened its manual:

```bash
man base64
```

Inside the manual, I searched for:

```text
/decode
```

This revealed two options:

| Option | Description |
| --- | --- |
| `-d` | Decode Base64 data |
| `--decode` | Long-form version of the decode option |

I also learned how to navigate manual pages:

| Key | Action |
| --- | --- |
| `/keyword` | Search for a keyword |
| `n` | Find the next match |
| `N` | Find the previous match |
| `q` | Quit the manual |

## 3. Understanding Command Syntax

One of the most important lessons was learning how to read the SYNOPSIS section of a Linux manual.

Example:

```text
base64 [OPTION]... [FILE]
```

| Component | Meaning |
| --- | --- |
| `base64` | Command being executed |
| `[OPTION]` | Optional command flag |
| `...` | Additional options may be supplied |
| `[FILE]` | Optional input filename |

Square brackets in documentation usually indicate optional arguments. They are not typed literally.

This helped me understand how to construct commands without memorizing every possible combination.

## 4. Understanding echo and Pipes

I also learned why `echo` and pipes are sometimes used when demonstrating commands.

Example:

```bash
echo "aGVsbG8=" | base64 -d
```

| Component | Purpose |
| --- | --- |
| `echo` | Prints the provided text |
| `"aGVsbG8="` | Base64-encoded example |
| `\|` | Passes output to the next command |
| `base64` | Base64 utility |
| `-d` | Decodes the input |

Expected output:

```text
hello
```

This example demonstrates decoding using text supplied directly in the terminal.

However, when the encoded data already exists in a file, using `echo` is unnecessary. The `base64` utility can read directly from a file.

**Key lesson:** Understand where a command receives its input before choosing how to run it.

## 5. A Better Linux Problem-Solving Process

Instead of guessing commands or immediately searching online, I practiced this workflow:

1. Read the challenge carefully.
2. Identify the file and data format.
3. Open the relevant Linux manual.
4. Find the operation needed.
5. Read the SYNOPSIS to understand the command's arguments.
6. Construct and test the command.
7. Verify the output.

This approach is useful beyond Bandit and applies to everyday Linux administration.

## 6. Real-World Applications

Base64 appears in several areas of cloud and infrastructure engineering.

- **Kubernetes:** Secret manifests commonly contain Base64-encoded values.
- **APIs:** Some authentication mechanisms use Base64 representations.
- **Linux administration:** Encoding and decoding data during troubleshooting.
- **Automation:** Handling encoded values in scripts and data exchanges.

Base64 does not provide confidentiality. Sensitive data still requires appropriate access controls and encryption.

## 7. Commands and Skills Learned

| Command or concept | What I learned |
| --- | --- |
| `whoami` | Verify the current Linux user |
| `man base64` | Find official command documentation |
| `-d` | Decode Base64 data |
| `--decode` | Long-form decoding option |
| `echo` | Print text to standard output |
| `\|` | Connect the output of one command to another |
| SYNOPSIS | Understand command usage syntax |
| Standard input | Understand how commands receive data |

## Biggest Takeaway

**Learning Linux is not about memorizing every command. It is about understanding how to discover commands, read documentation, and apply them to a problem.**

This lab helped me become more comfortable with Linux manual pages and taught me how Base64 decoding works.

## Credits

Lab provided by [OverTheWire Bandit](https://overthewire.org/wargames/bandit/).

This writeup documents the concepts learned without publishing passwords or challenge-specific solutions.
