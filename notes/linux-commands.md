# Linux Commands Learned

## ssh

Used to securely connect to a remote Linux system.

**Syntax:**

```bash
ssh username@host -p port
```

**Example:**

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

---

## ls

Lists files and directories.

**Examples:**

```bash
ls
```

```bash
ls -l
```

```bash
ls -la
```

**Notes:**

* `-l` = long listing format
* `-a` = show hidden files

---

## cat

Displays file contents.

**Syntax:**

```bash
cat filename
```

**Example:**

```bash
cat readme.txt
```

---

## file

Identifies the type of a file.

**Syntax:**

```bash
file filename
```

**Example:**

```bash
file data.txt
```

---

## find

Searches for files and directories.

**Examples:**

```bash
find . -type f
```

```bash
find . -size 1033c
```

```bash
find / -user bandit7 -group bandit6 -size 33c
```

---

## grep

Searches text for a pattern.

**Syntax:**

```bash
grep pattern filename
```

**Example:**

```bash
grep millionth data.txt
```

---

## strings

Extracts readable text from binary files.

**Example:**

```bash
strings data.txt
```

```bash
strings data.txt | grep =
```

---

## sort

Sorts lines alphabetically.

**Example:**

```bash
sort data.txt
```

---

## uniq

Removes or displays duplicate lines.

**Examples:**

```bash
uniq data.txt
```

```bash
sort data.txt | uniq -u
```

---

## base64

Encodes or decodes Base64 data.

**Decode:**

```bash
base64 -d data.txt
```

**Encode:**

```bash
echo "hello" | base64
```
