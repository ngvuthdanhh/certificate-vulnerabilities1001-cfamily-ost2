# 🧪 Lab: Use-After-Free (UAF)

## 🎯 Goal
- Demonstrate UAF bug
- Show how attacker can hijack program flow

## 🔬 Vulnerable Code
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct {
    char data[64];
} obj;

int main() {
    obj *o = malloc(sizeof(obj));
    strcpy(o->data, "Secret Data");

    free(o); // memory released
    printf("%s\n", o->data); // UAF

    return 0;
}
```
## 🚀 Exploitation

Attacker can reallocate memory at same address

Insert malicious object to control behavior

## 🛡️ Mitigations

Nullify pointers after free()

Hardened malloc implementations

Memory sanitizers

---
