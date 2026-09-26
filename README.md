# Huffman Compression

> A from-scratch **Huffman coding implementation in C** for lossless file compression.

This project implements the complete compression and decompression pipeline using Huffman coding.

```text
Input
  ↓
Frequency Analysis
  ↓
Huffman Tree
  ↓
Variable-Length Codes
  ↓
Bit-Packed Output
```

## Implementation

* 256-byte frequency table
* Huffman tree built by repeatedly combining the two least-frequent nodes
* Variable-length prefix codes generated from tree traversal
* Compressed bits packed into bytes
* Frequency information stored with the encoded data so the tree can be reconstructed during decompression

The implementation uses dynamic C data structures including linked lists and binary trees.

## Build

```bash
gcc client_pro.c pro.c pro2.c -o huffman
./huffman
```

### Files

```text
client_pro.c   # Program entry point
pro.c          # Compression
pro2.c         # Decompression
pro.h          # Data structures and declarations
```
