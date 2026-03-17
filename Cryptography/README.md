# Cryptography

This folder contains implementations of **cryptographic algorithms** and utilities for encrypting, decrypting, and hashing data.

## What is Cryptography?

Cryptography is the practice of securing information so that only intended recipients can read it. Modern cryptographic algorithms underpin HTTPS, secure messaging, digital signatures, and password storage.

## Files

| File | Description |
|------|-------------|
| `Cryptography.h` | Cryptographic algorithm implementations |
| `CryptographyTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the cryptography tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
