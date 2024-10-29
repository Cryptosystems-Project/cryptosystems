# Cryptosystems Package

## Overview
The `cryptosystems` package offers a robust suite of classes and functions for both symmetric and asymmetric encryption, as well as hashing functionalities. Designed for seamless encryption, decryption, and cryptographic operations, this package is lightweight and efficient, relying solely on Python’s built-in libraries: `os` and `hashlib`. With all cryptographic logic implemented from scratch, cryptosystems provides a streamlined, dependency-free solution, ensuring consistency and reliability across different environments as well as Python versions.

## Key Advantages
- **Dependency-Free** 🚫📦: Operates solely on Python's built-in modules, eliminating the need for external libraries.
- **Version Stability** 🔒📅: Crafted to maintain consistent functionality across Python versions.
- **Optimized for Performance** ⚡⚙️: Built from scratch for efficient and consistant cryptographic operations.
- **Lightweight Codebase** 🪶💻: Minimalistic design ensures a low overhead and straightforward integration.
- **Reliability and Security** 🔐🛡️: Ensures robust encryption/decryption and hashing without reliance on third-party modules.
- **Comprehensive Cryptosystem Support** 🔄🔑: Offers a full suite of symmetric, asymmetric, and hashing methods.

## Installation
To install the package, simply clone the repository and install the dependencies:
```bash
git clone https://github.com/ishan-surana/cryptosystems.git
cd cryptosystems
pip install -r requirements.txt
```

## Usage

**<details><summary> Symmetric Ciphers (Basic Cryptosystems)**</summary>

#### AdditiveCipher
```python
from cryptosystems import AdditiveCipher

cipher = AdditiveCipher(3)
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: 'Khoor Zruog'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

#### MultiplicativeCipher
```python
from cryptosystems import MultiplicativeCipher

cipher = MultiplicativeCipher(5)
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: 'Czggj Rjmgy'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

#### AffineCipher
```python
from cryptosystems import AffineCipher

cipher = AffineCipher(5, 8)
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: 'Rclla Oaplx'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

#### HillCipher
```python
from cryptosystems import HillCipher

cipher = HillCipher([[3, 3], [2, 5]])
ciphertext = cipher.encrypt("HelloWorld")
print(ciphertext)  # Output: 'HiozeIpjql'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'HelloWorld'
```

#### VigenereCipher
```python
from cryptosystems import VigenereCipher

cipher = VigenereCipher("key")
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: 'Rijvs Uyvjk'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

#### PlayfairCipher
```python
from cryptosystems import PlayfairCipher

cipher = PlayfairCipher("key")
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: 'Dahak Ldskn'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

#### AutoKeyCipher
```python
from cryptosystems import AutoKeyCipher

cipher = AutoKeyCipher("key")
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: 'Rijss Hzfhr'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

</details>

**<details><summary> Symmetric Ciphers (Advanced Cryptosystems)**</summary>

#### DES
```python
from cryptosystems import DES

cipher = DES("password")
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: b'\xf4\\V\x1a\xc7S\xb7\xdeZ\xc1\xe9\x14\n\x15Y\xe8'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

#### AES
```python
from cryptosystems import AES

cipher = AES("passwordpassword")
ciphertext = cipher.encrypt("Hello World")
print(ciphertext)  # Output: b'\x9cHS\xc2\x00\x0c\xba\x82Bj\x90\xc3t|4}'
plaintext = cipher.decrypt(ciphertext)
print(plaintext)  # Output: 'Hello World'
```

</details>

**<details><summary> Asymmetric Ciphers**</summary>

#### RSA
```python
from cryptosystems import RSA

rsa = RSA(1024)
ciphertext = rsa.encrypt(123)
print(ciphertext)  # Output: 1234567890
plaintext = rsa.decrypt(ciphertext)
print(plaintext)  # Output: 123
```

#### ElGamal
```python
from cryptosystems import ElGamal

elgamal = ElGamal(1024)
ciphertext = elgamal.encrypt(123)
print(ciphertext)  # Output: (123, 123)
plaintext = elgamal.decrypt(ciphertext)
print(plaintext)  # Output: 123
```

#### Rabin
```python
from cryptosystems import Rabin

rabin = Rabin(1024)
ciphertext = rabin.encrypt(123)
print(ciphertext)  # Output: 1234567890
plaintext = rabin.decrypt(ciphertext)
print(plaintext)  # Output: 123
```

#### Paillier
```python
from cryptosystems import Paillier

paillier = Paillier(1024)
ciphertext = paillier.encrypt(123)
print(ciphertext)  # Output: 1234567890
plaintext = paillier.decrypt(ciphertext)
print(plaintext)  # Output: 123
```

#### DiffieHellman
```python
from cryptosystems import DiffieHellman

diffiehellman = DiffieHellman()
shared_secret = diffiehellman.getSharedSecret()
print(shared_secret)  # Output: 1234567890
```

</details>

**<details><summary> Hash Functions**</summary>

#### MD5
```python
from cryptosystems import MD5

md5 = MD5()
hash_value = md5.hash("Hello World")
print(hash_value)  # Output: 'b10a8db164e0754105b7a99be72e3fe5'
```

#### SHA256
```python
from cryptosystems import SHA256

sha256 = SHA256()
hash_value = sha256.hash("Hello World")
print(hash_value)  # Output: 'a591a6d40bf420404a011733cfb7b190d62c65bf0bcda32b57b277d9ad9f146e'
```

</details>

**<details><summary> Utility Functions**</summary>

#### getRandomInteger
```python
from cryptosystems import getRandomInteger

random_int = getRandomInteger(1024)
print(random_int)
```

#### getRandomRange
```python
from cryptosystems import getRandomRange

random_range = getRandomRange(1, 100)
print(random_range)
```

#### isPrime
```python
from cryptosystems import isPrime

prime_check = isPrime(17)
print(prime_check)  # Output: True
```

#### getPrime
```python
from cryptosystems import getPrime

prime_number = getPrime(1024)
print(prime_number)
```

</details>

## License
This project is licensed under the Apache License - see the [LICENSE](LICENCE) file for details.

## Authors
- **Ishan Surana** - *Inception, implementation and testing* - [GitHub](https://github.com/ishan-surana)

## Acknowledgments
- PyCryptodome, for the logic of functions in the [functions submodule](cryptosystems/functions.py)