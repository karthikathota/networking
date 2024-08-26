# Hashing

Hashing is a technique used in computing to transform input data into a 
fixed-size string of characters, which is typically a sequence of numbers and letters. This fixed-size string is known as a hash value or hash code. Hashing is generally done to secure passwords and other 
sensitive information to secure the users data.

## How hashing works?

### Hash Function:-
The process begins with a hash function, a special algorithm that takes an input (or "message") and produces a hash value. 
The hashed value cannot be converted again into the original value i.e once an hash is created for an input we cannot again reconstruct the input from the hashed value.

### Fixed Size Output

No matter how large or small the input data is, the output hash is always of a fixed size.  
Example:-  SHA-256 hash function always produces a 256-bit hash value

### Unique

A good hash function minimizes the likelihood of different inputs producing the same hash value i.e collision.  

Example:-
```python
import hashlib

def hash_string(input_string):
    encoded_string = input_string.encode()
    sha256_hash = hashlib.sha256()
    sha256_hash.update(encoded_string)
    hex_digest = sha256_hash.hexdigest()
    return hex_digest

input_string = "Test123"
hashed_string = hash_string(input_string)
print(f"SHA-256 hash: {hashed_string}")

# Output :- SHA-256 hash: d9b5f58f0b38198293971865a14074f59eba3e82595becbe86ae51f1d9f1f65e
```

```python
encoded_string = input_string.encode()
```

This step is necessary as the hash fucntion requires byte input.

# Encryption

Encryption is a process of converting plaintext (readable data) into ciphertext (encoded data) using an algorithm and a key.  
Unlike hashing in encryption we can get the original value back by decrypting the ciphertext.  
One of the main part of encryption and decryption is KEY. It is a piece of information used by encryption and decryption algorithms. It’s critical for the security of the encrypted data.  
There are 2 types of encryptions:-  
1) Symmetric Encryption  
2)Asymmetric Encryption  

### Symmetric Encryption

In symmetric encryption we use same key for both encryption and decryption.  
Example:- AES, DES  

```python

```
### Asymmetric Encryption

In asymmetric encryption we use 2 types of keys i.e a public key and a private key. Public key is used for encryption and Private key is used for decryption.  
