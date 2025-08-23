# ➕ Integer Overflows

## Description
An arithmetic operation exceeds the representable range of the type.

## Example
```c
int len = input * 4;
char *buf = malloc(len);
```

If input is very large → integer wraps → too little memory allocated → buffer overflow.

- Defenses

Use safe libraries (size_t).

Explicit bounds checking.

---
