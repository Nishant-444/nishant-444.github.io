---
layout: essay
type: essay
title: "Why Text Files are Slow: Optimizing C++ Banking Ops"
date: 2024-02-15
published: true
labels:
  - C++
  - Systems Programming
  - Optimization
  - Binary I/O
---

# 300% Faster: Text vs. Binary Serialization

When building **BankEase**, a banking simulation engine, I initially used standard text file I/O (`fstream` with `<<` operators) to store user records. It was readable, but slow.

As the dataset grew to thousands of accounts, the overhead of parsing text (converting `"1000.50"` string to `1000.50` float) became a bottleneck.

### The Solution: Binary I/O

I rewrote the storage engine to use **Binary Serialization**. Instead of writing human-readable characters, I dumped the raw memory of the C++ objects directly to the disk.

```cpp
// Old Way (Text) - Slow parsing
file << account.id << " " << account.balance << endl;

// New Way (Binary) - Raw memory copy
file.write(reinterpret_cast<char*>(&account), sizeof(Account));
```
