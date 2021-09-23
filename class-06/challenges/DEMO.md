# Ops Challenge - File Encryption Script Part 1 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python
# Encrypt a single string

# Import Libraries

from cryptography.fernet import Fernet

# Declare Functions

def write_key():
    # Generates a key and save it into a file
    key = Fernet.generate_key()
    with open("key.key", "wb") as key_file:
        key_file.write(key)

def load_key():
    # Loads the key from the current directory named `key.key`
    return open("key.key", "rb").read()

# Main

# Generate and write a new key
write_key()

# load the previously generated key
key = load_key()
print("Key is "+str(key.decode('utf-8')))

message = "hello friend".encode()
print("Plaintext is "+str(message.decode('utf-8')))

# Initialize the Fernet class
f = Fernet(key)

# Encrypt the message
encrypted = f.encrypt(message)

# Print how it looks
print("Ciphertext is "+encrypted.decode('utf-8'))
```
"DEMO.md" 45L, 1015C                                                                                                                                                 1,1           Top
