# Huffman Compression

> A from-scratch **Huffman coding implementation in C** for lossless file compression.

This project implements both **compression and decompression** using Huffman coding, focusing on the underlying data structures and bit-level representation rather than relying on a compression library.

## How It Works

```text
Input File
    ↓
Frequency Analysis
    ↓
Build Huffman Tree
    ↓
Generate Prefix Codes
    ↓
Pack Bits into Bytes
    ↓
Compressed Data
```

Characters that occur frequently receive shorter bit sequences, while less frequent characters receive longer sequences. The resulting variable-length codes are prefix-free, allowing the original data to be reconstructed without ambiguity.

## Implementation

* Frequency table for all **256 possible byte values**
* Binary Huffman tree built by repeatedly combining the two least-frequent nodes
* Variable-length codes generated from tree traversal
* Bit-level packing of Huffman codes into bytes
* Frequency information stored with the encoded data to reconstruct the tree during decompression
* Dynamic C data structures including **linked lists and binary trees**

## Build & Run

```bash
gcc client_pro.c pro.c pro2.c -o huffman
./huffman
```

## Project Structure

```text
client_pro.c   # Program entry point
pro.c          # Compression and Huffman tree construction
pro2.c         # Decompression
pro.h          # Data structures and declarations
```
