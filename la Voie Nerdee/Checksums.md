---
banner_y: 44.4%
---
A *checksum* is a short, unique code generated from a block of data to verify its integrity.
It acts as a digital fingerprint that represents the exact state of a file.

Comparing checksums helps detecting errors that may occur during the file transmission or [[Bit rot|storage]].

The process that generates the checksum is called a *checksum algorithm*.
A good checksum algorithm usually outputs a significantly different value, even for small changes made to the input.

A checksum confirms integrity, but not authenticity. An attacker could replace a file and generate a matching checksum.
That’s why distributions pair checksums with [[GnuPG|GPG signatures]]: the checksum proves the file hasn’t changed, the signature proves it came from the right source.

## #️⃣ Common algorithms

### SHA-512
- Modern algorithm, protected against brute-force attacks
- Produces a 512-bit hash
- Faster on 64-bit systems

### SHA-256
- Also modern & secure algorithm used in blockchain
- Produces a 256-bit hash
- Faster on 32-bit systems

### MD5, SHA-1, CRC32
- Legacy algorithms which are mostly deprecated today for security reasons 


## ☑️ Usage

- Verify the ISO checksum:
```bash
# Make sure the checksum file is in the same directory as the ISO file
sha256sum --check --ignore-missing <sum_file> # same for sha512sum, md5sum etc.
```





[^1]: Sources:
		https://en.wikipedia.org/wiki/Checksum
		https://linuxsecurity.com/features/what-are-checksums-why-should-you-be-using-them
