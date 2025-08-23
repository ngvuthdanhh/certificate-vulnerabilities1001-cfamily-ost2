# 🧪 Lab: Buffer Overflow

## 🎯 Goal
- Understand stack-based buffer overflows
- Overwrite return address
- Gain shell execution

## 🔬 Vulnerable Code
```c
#include <stdio.h>
#include <string.h>

void vuln() {
    char buf[64];
    gets(buf); // unsafe
}

int main() {
    vuln();
    return 0;
}
```
## 🚀 Exploitation

Input longer than 64 bytes overwrites return address

Redirect execution flow to injected shellcode

Example payload structure:

```css
[A * 64] + [EIP overwrite] + [NOP sled] + [Shellcode]
```

🛡️ Mitigations

Replace gets() with fgets()

Enable stack canaries

DEP + ASLR


---
