# 📌 Buffer Overflow

## What It Is
A buffer overflow occurs when writing data beyond the allocated memory region.

## Example
```c
char buf[16];
gets(buf);  // unsafe, no bounds checking
```
- Key Concepts

Stack smashing

Saved EIP overwrite

Shellcode injection

- Defenses

Stack canaries

DEP (Data Execution Prevention)

ASLR


---
