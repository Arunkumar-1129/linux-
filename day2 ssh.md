# chmod

## What is chmod?

`chmod` stands for **Change Mode**.

It is used to change the permissions of files and directories.

---

## Why is chmod needed?

Linux protects every file using permissions.

There are three categories:

```
Owner
Group
Others
```

Each category can have

```
Read (r)
Write (w)
Execute (x)
```

---

## Permission Values

| Permission | Value |
|------------|------:|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

---

## Permission Representation

```
rwxr-xr-x
```

Breakdown

```
rwx
```

Owner

```
r-x
```

Group

```
r-x
```

Others

---

## Numeric Representation

```
rwx
```

4+2+1 = 7

```
r-x
```

4+1 = 5

```
r-x
```

4+1 = 5

Therefore

```
755
```

---

## Syntax

```bash
chmod [permissions] file
```

---

## Example

```bash
chmod 755 script.sh
```

---

## Output

```
(No output)
```

Verify

```bash
ls -l
```

Output

```text
-rwxr-xr-x
```

---

## Symbolic Method

Give execute permission

```bash
chmod +x script.sh
```

Remove execute permission

```bash
chmod -x script.sh
```

Give write permission

```bash
chmod u+w file.txt
```

Remove write permission

```bash
chmod g-w file.txt
```

---

## Interview Questions

Q. Difference between

```
chmod 777
```

and

```
chmod 755
```

777

Everyone

```
Read
Write
Execute
```

755

Owner

```
Read
Write
Execute
```

Group

```
Read
Execute
```

Others

```
Read
Execute
```

---

## Common Mistakes

❌

```
chmod 999 file
```

Invalid permission.

---

## Best Practice

Never use

```
777
```

unless absolutely necessary.
