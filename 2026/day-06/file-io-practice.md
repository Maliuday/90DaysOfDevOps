# File I/O Practice

## File Creation

### Command

```bash
touch notes.txt
```

Created an empty file named notes.txt.

---

## Writing Data

### Command

```bash
echo "I am learning Linux." > notes.txt
```

Added the first line to the file.

### Command

```bash
echo "Linux is important for DevOps." >> notes.txt
```

Appended the second line.

### Command

```bash
echo "I practice every day." >> notes.txt
```

Appended the third line.

---

## Using tee

### Command

```bash
echo "This line was added using tee command." | tee -a notes.txt
```

Displayed and appended text at the same time.

---

## Reading the File

### Command

```bash
cat notes.txt
```

Displayed the complete file contents.

### Command

```bash
head -n 2 notes.txt
```

Displayed the first two lines.

### Command

```bash
tail -n 2 notes.txt
```

Displayed the last two lines.

---

## What I Learned

* How to create files using touch.
* Difference between > and >> redirection.
* How to read files using cat.
* How to view file sections using head and tail.
* How to use tee for writing and displaying output.
