# StringAlgorithms

This folder contains implementations of **string processing algorithms** for searching, indexing, and transforming text.

## Algorithms Included

### Substring Search (`SubstringSearch.h`)
Finds all occurrences of a pattern within a longer text more efficiently than the naive O(nm) approach:
- **Knuth-Morris-Pratt (KMP)**: O(n + m) by precomputing a failure function to avoid redundant comparisons.
- **Boyer-Moore**: Often sublinear in practice by skipping sections of the text.
- **Rabin-Karp**: Uses hashing for multi-pattern search; O(n + m) average.

### Suffix Array (`SuffixArray.h`)
A sorted array of all suffixes of a string. Enables O(m log n) substring search, finding the longest repeated substring, and computing longest common prefixes — all in O(n log n) or O(n) construction time. Used in bioinformatics (genome alignment), data compression, and full-text search.

### Regular Expressions (`RegEx.h`)
Matches strings against patterns specified with wildcards, character classes, and quantifiers. Implemented using NFA/DFA construction for efficient linear-time matching.

### String Diff (`Diff.h`)
Computes the **longest common subsequence (LCS)** and edit distance (Levenshtein distance) between two strings or sequences. The diff output shows which lines were added, removed, or unchanged — the basis of the Unix `diff` command and version control systems.

### Rank/Select (`RankSelect.h`)
Succinct data structures that support:
- **Rank(i)**: Count the number of 1-bits in the first i positions
- **Select(k)**: Find the position of the k-th 1-bit

These are used in compressed text indexes, wavelet trees, and space-efficient data structures.

## Files

| File | Description |
|------|-------------|
| `SubstringSearch.h` | Substring search algorithms (KMP, Boyer-Moore, Rabin-Karp) |
| `SuffixArray.h` | Suffix array construction and queries |
| `RegEx.h` | Regular expression matching |
| `Diff.h` | LCS, edit distance, and diff |
| `RankSelect.h` | Rank and select on bit sequences |
| `StringAlgorithmsTestAuto.h` | Automated test helpers |
| `test.cpp` | Test driver for string algorithms |
| `testRankSelect.cpp` | Test driver for rank/select |

## Usage

Compile and run the test files:

```bash
g++ -O2 -o test test.cpp && ./test
g++ -O2 -o testRankSelect testRankSelect.cpp && ./testRankSelect
```
