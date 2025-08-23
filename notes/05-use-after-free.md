# 🗑️ Use-After-Free (UAF)

## Description
Accessing memory after it has been freed.

## Example
```c
char *buf = malloc(100);
free(buf);
strcpy(buf, "test"); // UAF
```
- Risks

Arbitrary code execution

Privilege escalation

- Defenses

Set pointers to NULL after free

Use memory-safe languages


---
