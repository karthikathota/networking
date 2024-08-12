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

