# 🖨️ Format String Vulnerabilities

## Description
Occurs when user input is passed directly into formatted functions (`printf`, `sprintf`, etc.).

## Example
```c
printf(user_input);   // dangerous
```

## Exploitation

Arbitrary read (leak memory)

Arbitrary write (%n specifier)

Control hijack

- Defenses

Always use format specifiers (printf("%s", user_input)).

Compiler warnings (-Wformat).

---
