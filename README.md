# SpellChecker
A C++ program implementing a Bloom Filter for fast spell-checking using a dictionary file. It hashes words with 6 functions, sets corresponding bits in a bit vector, and checks for probable word existence. Optimized with modular exponentiation and bitwise operations for efficient storage and lookup.
## Features

- Custom `BitVector` class for efficient bit manipulation.
- Bloom Filter with 6 hash functions for word insertion and lookup.
- Case-insensitive word processing.
- Loads words from a dictionary file to build the filter.
- Interactive console input for real-time spell checking.
- Progress display during dictionary loading.

---

## How It Works

1. Reads words from a dictionary file (`dictionary.txt`).
2. Inserts each word into the Bloom Filter by setting bits at positions generated by multiple hash functions.
3. To check spelling, hashes the input word and checks the corresponding bits.
4. If all bits are set, the word is *probably* in the dictionary (may include false positives).
5. If any bit is not set, the word is *definitely* not in the dictionary.

---

## Usage

1. Place your dictionary file at the path specified in the code (default: `C:\\Users\\sajin\\OneDrive\\Desktop\\dictionary.txt`).
2. Compile the program with a C++11 (or higher) compatible compiler.
3. Run the executable.
4. Enter words or sentences to check their spelling.
5. Type `n` when asked if you want to continue to exit the program.

## Requirements

- C++11 or higher compiler.
- Windows OS (due to usage of `<Windows.h>` and `system("color 0e")`).
- Dictionary file with one word per line.

## Notes

- Bloom Filter may yield false positives but never false negatives.
- Filter size is set to 728,000 bits; adjust in the source if needed.
- Modify the dictionary path in the code as per your file location.
