# 🛡️ Secure Coding Playbook

## 🎯 Objective
Provide practical coding guidelines to reduce software implementation vulnerabilities in C-family languages.

## ✅ Best Practices
- Always **validate input length** (avoid `gets`, `scanf` without size).
- Use **safe string functions** (`strncpy`, `snprintf`).
- Apply **memory bounds checks** for arrays and buffers.
- Initialize all pointers and variables before use.
- Free allocated memory **once only** and set pointer to `NULL`.

## 🔧 Compiler & Tooling
- Enable compiler flags: `-Wall -Wextra -Wformat -fstack-protector-all`
- Use static analyzers: `clang-tidy`, `cppcheck`
- Apply runtime checkers: `ASAN`, `Valgrind`

## 🛡️ Defenses in Depth
- Enable **ASLR, DEP/NX, stack canaries**
- Prefer **memory-safe libraries** (e.g., `libsafe`)
- Regular **code audits & fuzzing**
