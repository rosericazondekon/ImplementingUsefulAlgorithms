# ErrorCorrectingCodes

This folder contains implementations of **error detection and correction codes** used to protect data from corruption during storage or transmission.

## Algorithms Included

### CRC – Cyclic Redundancy Check (`CRC.h`)
CRC is a fast error-detection algorithm that appends a short checksum to data. The receiver recomputes the checksum and compares it to detect transmission errors. CRC is used in Ethernet, ZIP files, and disk storage.

### LDPC – Low-Density Parity Check (`LDPC.h`)
LDPC codes are powerful error-correcting codes that can recover data even when a significant portion of it is corrupted. They are used in modern wireless communications (5G, Wi-Fi), DVB-S2 satellite broadcasting, and storage devices.

### Reed-Solomon Codes (`ReedSolomon.h`)
Reed-Solomon is a widely-used error-correcting code capable of correcting both erasures and errors. It is the basis for error correction in CDs, DVDs, QR codes, and deep-space communications (e.g., Voyager probes).

## Files

| File | Description |
|------|-------------|
| `CRC.h` | Cyclic Redundancy Check implementation |
| `LDPC.h` | Low-Density Parity Check codes |
| `ReedSolomon.h` | Reed-Solomon error-correcting codes |
| `ErrorCorrectingCodesTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |

## Usage

Compile and run `test.cpp` to exercise the error-correcting code tests:

```bash
g++ -O2 -o test test.cpp && ./test
```
