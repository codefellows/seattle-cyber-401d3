# Ops Challenge: File Encryption

## Demo Code

Here is the code that was demonstrated in class.

```powershell
# Encrypt a file
(Get-Item –Path "C:\Users\administrator\Desktop\filename").Encrypt()

# Decrypt a file
(Get-Item –Path "C:\Users\administrator\Desktop\filename").Decrypt()

# Generate an encrypted string from a plaintext string
"P@ssword1" | ConvertTo-SecureString -AsPlainText -Force | ConvertFrom-SecureString

# Generate a hash without specifying the algorithm
Get-FileHash "C:\Users\administrator\Desktop\filename" 

# Specify SHA256 algorithm explicitly
Get-FileHash "C:\Users\administrator\Desktop\filename" -Algorithm SHA256
```
