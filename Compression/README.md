# Compression

This folder contains implementations of classic **lossless data compression** algorithms.

## Algorithms Included

### Huffman Coding (`HuffmanTree.h`, `StaticCodes.h`)
Huffman coding is a greedy algorithm that assigns shorter binary codes to more frequent symbols and longer codes to less frequent ones. This minimizes the total number of bits needed to represent the data. It is widely used in formats like JPEG, MP3, and ZIP.

### LZW – Lempel-Ziv-Welch (`LZW.h`)
LZW is a dictionary-based compression algorithm that replaces repeated substrings with short codes. It is used in the GIF image format and the Unix `compress` utility. The algorithm builds its dictionary on-the-fly as it encodes or decodes data.

### Stream Utilities (`Stream.h`, `Compression.h`)
Helper classes for reading and writing compressed bit streams and coordinating the compression pipeline.

## Files

| File | Description |
|------|-------------|
| `Compression.h` | Top-level compression interface |
| `Compressor.cpp` | Compressor implementation |
| `HuffmanTree.h` | Huffman tree and encoding/decoding logic |
| `LZW.h` | Lempel-Ziv-Welch compression algorithm |
| `StaticCodes.h` | Static (pre-computed) Huffman code tables |
| `Stream.h` | Bit-stream reader/writer utilities |
| `CompressionTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver |
| `README.txt` | Notes on downloading test data from Princeton |

## Usage

Compile and run `test.cpp` to exercise the compression tests:

```bash
g++ -O2 -o test test.cpp && ./test
```

> **Note:** Some tests require sample data files. See `README.txt` for download instructions.
