# Linux Command Reference

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

**Important options:**

| Option | Meaning                         |
| ------ | ------------------------------- |
| -p     | Specify the port number         |
| -i     | Use a specific private key file |
| -v     | Enable verbose/debug output     |

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

**Important options:**

| Option | Meaning                         |
| ------ | ------------------------------- |
| -l     | Long listing format             |
| -a     | Show hidden files               |
| -h     | Human-readable file sizes       |
| -R     | Recursively list subdirectories |

---

## cat

Displays file contents.

**Syntax:**

```bash
cat filename
```

**Example:**

```bash
cat notes.txt
```

**Important options:**

| Option | Meaning                     |
| ------ | --------------------------- |
| -n     | Show line numbers           |
| -b     | Number non-empty lines      |
| -E     | Show end-of-line characters |

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

**Important options:**

| Option | Meaning        |
| ------ | -------------- |
| -b     | Brief output   |
| -i     | Show MIME type |

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

**Important options:**

| Option  | Meaning                     |
| ------- | --------------------------- |
| -name   | Search by filename          |
| -type f | Files only                  |
| -type d | Directories only            |
| -size   | Search by size              |
| -user   | Search by owner             |
| -group  | Search by group             |
| -mtime  | Search by modification time |

---

## grep

Searches text using patterns.

**Syntax:**

```bash
grep pattern filename
```

**Example:**

```bash
grep millionth data.txt
```

**Important options:**

| Option | Meaning                 |
| ------ | ----------------------- |
| -i     | Ignore case             |
| -n     | Show line numbers       |
| -r     | Search recursively      |
| -v     | Show non-matching lines |
| -c     | Count matching lines    |

---

## strings

Extracts readable text from binary files.

**Examples:**

```bash
strings data.txt
```

```bash
strings data.txt | grep =
```

**Important options:**

| Option    | Meaning               |
| --------- | --------------------- |
| -n NUMBER | Minimum string length |
| -a        | Scan entire file      |

---

## sort

Sorts lines alphabetically.

**Example:**

```bash
sort data.txt
```

**Important options:**

| Option | Meaning                     |
| ------ | --------------------------- |
| -r     | Reverse order               |
| -n     | Numeric sort                |
| -u     | Remove duplicate lines      |
| -k     | Sort using a specific field |

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

**Important options:**

| Option | Meaning                   |
| ------ | ------------------------- |
| -u     | Show unique lines only    |
| -d     | Show duplicate lines only |
| -c     | Count occurrences         |

---

## base64

Encodes or decodes Base64 data.

**Encode:**

```bash
echo "hello" | base64
```

**Decode:**

```bash
base64 -d data.txt
```

**Important options:**

| Option | Meaning                 |
| ------ | ----------------------- |
| -d     | Decode Base64 data      |
| -w     | Set line wrapping width |

---

## Commands Practiced Through Bandit

* ssh
* ls
* cat
* file
* find
* grep
* strings
* sort
* uniq
* base64

These commands were learned and practiced while completing the OverTheWire Bandit wargame.
