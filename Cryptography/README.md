# Cryptography

This folder contains implementations of **cryptographic algorithms** and utilities for encrypting, decrypting, and hashing data.

## What is Cryptography?

Cryptography is the practice of securing information so that only intended recipients can read it. Modern cryptographic algorithms underpin HTTPS, secure messaging, digital signatures, and password storage.

## Algorithms Included

### ARC4 Stream Cipher (`Cryptography.h`)
ARC4 (also known as RC4) is a symmetric key stream cipher. It generates a pseudo-random byte stream (keystream) from a secret key, then XORs it with the plaintext to produce ciphertext. Decryption is identical — XOR the ciphertext with the same keystream to recover the original data. ARC4 is fast and simple; it has been widely used in SSL/TLS and WEP, though it is now considered legacy.

The implementation uses **Xorshift** to randomize the key before initializing the ARC4 state, reducing key-scheduling weaknesses.

### CRC32 Integrity Check (`Cryptography.h`, via `ErrorCorrectingCodes/CRC.h`)
A 32-bit Cyclic Redundancy Check is appended to data before encryption to verify integrity on decryption. If the decrypted CRC does not match the recomputed one, the message was corrupted or tampered with.

### `simpleEncrypt` / `simpleDecrypt`
Convenience functions that combine the above primitives into a complete encrypt-then-MAC scheme:

1. **`simpleEncrypt(data, key)`**  
   - Computes a CRC32 checksum of the plaintext and appends it.  
   - Applies ARC4 (with a random time-based seed mixed into the key) to encrypt the combined data.  
   - Appends the random seed in plaintext so the receiver can reconstruct the keystream.

2. **`simpleDecrypt(code, key)`**  
   - Extracts the seed, reconstructs the ARC4 keystream, and decrypts.  
   - Verifies the embedded CRC32; returns the plaintext together with a boolean indicating whether integrity check passed.

## Files

| File | Description |
|------|-------------|
| `Cryptography.h` | ARC4 stream cipher, CRC32 integrity check, simpleEncrypt/simpleDecrypt |
| `CryptographyTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the cryptography tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
