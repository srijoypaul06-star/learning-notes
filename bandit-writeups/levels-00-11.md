# OverTheWire Bandit Notes

These are my notes while learning Linux and basic cybersecurity concepts through the OverTheWire Bandit wargame.

## Level 0 → 1

**Objective:** Connect to the Bandit server and get the password for the next level.

**Command used:**

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

**My takeaway:** This was my first time connecting to a remote Linux machine using SSH. I learned that SSH provides secure remote access through the terminal.

## Level 1 → 2

**Objective:** Read the password stored in a file named `-`.

**Command used:**

```bash
cat ./-
```

**My takeaway:** I learned that files with special names sometimes need to be referenced using `./`.

## Level 2 → 3

**Objective:** Read the file that contains spaces in its name.

**Command used:**

```bash
cat "spaces in this filename"
```

**My takeaway:** Filenames containing spaces must be wrapped in quotes or escaped with backslashes.

## Level 3 → 4

**Objective:** Find the hidden file inside the `inhere` directory.

**Commands used:**

```bash
ls -la
cat .hidden
```

**My takeaway:** Files beginning with a dot (`.`) are hidden by default. Using `ls -la` displays hidden files.

## Level 4 → 5

**Objective:** Find the only human-readable file among multiple files.

**Command used:**

```bash
file ./*
```

**My takeaway:** The `file` command identifies file types based on their contents rather than their extensions.

## Level 5 → 6

**Objective:** Find a file matching specific size and permission requirements.

**Command used:**

```bash
find . -type f -size 1033c
```

**My takeaway:** The `find` command can search for files using attributes such as size, type, ownership, and permissions.

## Level 6 → 7

**Objective:** Find a file owned by a specific user and group.

**Command used:**

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

**My takeaway:** I learned how to suppress error messages using `2>/dev/null` to keep output clean.

## Level 7 → 8

**Objective:** Find the password next to the word "millionth".

**Command used:**

```bash
grep millionth data.txt
```

**My takeaway:** `grep` makes it easy to search large files for specific words or patterns.

## Level 8 → 9

**Objective:** Find the only line that appears once.

**Command used:**

```bash
sort data.txt | uniq -u
```

**My takeaway:** I learned how pipes (`|`) connect commands together and why sorting is important before using `uniq`.

## Level 9 → 10

**Objective:** Find the password hidden inside binary data.

**Command used:**

```bash
strings data.txt | grep =
```

**My takeaway:** The `strings` command extracts readable text from files containing binary data.

## Level 10 → 11

**Objective:** Decode Base64 encoded data.

**Command used:**

```bash
base64 -d data.txt
```

**My takeaway:** Base64 is an encoding format, not encryption, and can be easily decoded.

## Overall Progress

So far I have learned and practiced:

* ssh
* cat
* ls
* file
* find
* grep
* strings
* sort
* uniq
* base64

Bandit has helped me become more comfortable working in Linux and solving problems through the terminal.
