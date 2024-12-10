# AES/Vigenère Cipher Implementation

A Python implementation of AES (Advanced Encryption Standard) with an option to replace the SubBytes operation with a Vigenère cipher.

## Features

- Standard AES-128 implementation
- Hybrid mode replacing SubBytes with Vigenère cipher
- Case-preserving Vigenère cipher implementation
- Support for file input/output
- Command-line interface

## Installation

```bash
git clone <repository-url>
cd <repository-name>
```

## Command Line Arguments

```bash
usage:

ciphers.py

 [-h] [--cipher {aes,vigenere}] [--master_key MASTER_KEY]
                  [--plaintext PLAINTEXT] [-i] [-o OUTPUT]
```

### Options

- `-h, --help`: Show help message and exit
- `--cipher {aes,vigenere}`: Select cipher type (default: aes)
- `--master_key MASTER_KEY`: Encryption key
  - For AES: 128-bit hex value
  - For Vigenère: ASCII string
- `--plaintext PLAINTEXT`: Input text to encrypt
- `-i, --stdin`: Read input from stdin
- `-o OUTPUT, --output OUTPUT`: Write output to specified file

### Examples

```bash
# Show help
python ciphers.py -h

# Use Vigenère with custom key
python ciphers.py --cipher vigenere --master_key "MYKEY" --plaintext "Hello"

# Read from file, write to custom output
cat input.txt | python ciphers.py -i -o result.txt
```

## Usage

### Basic Usage

```bash
# Standard AES encryption
python ciphers.py --plaintext "Hello World"

# AES with Vigenère SubBytes
python ciphers.py --cipher vigenere --plaintext "Hello World"
```

### Input/Output Options

```bash
# Read from stdin
echo "Hello World" | python ciphers.py -i

# Specify output file
python ciphers.py --plaintext "Hello World" -o output.txt

# Default output files: encrypted_[method].txt and decrypted_[method].txt
```

## Implementation Details

Plan for README.md:

1. Project description
2. Features
3. Installation
4. Usage examples
5. Implementation details

```markdown
# AES/Vigenère Cipher Implementation

A Python implementation of AES (Advanced Encryption Standard) with an option to replace the SubBytes operation with a Vigenère cipher.

## Features

- Standard AES-128 implementation
- Hybrid mode replacing SubBytes with Vigenère cipher
- Case-preserving Vigenère cipher implementation
- Support for file input/output
- Command-line interface
