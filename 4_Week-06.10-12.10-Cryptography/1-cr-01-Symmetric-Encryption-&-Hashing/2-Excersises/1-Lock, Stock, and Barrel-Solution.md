# Lock, Stock, and Barrel

**Course:** Cyber Security Analyst - Symmetric Encryption & Hashing | **Date:** 06 October 2025

---

## Task

Use `openssl` to encrypt `message.txt`, observe the ciphertext, trigger a failed decryption with the wrong password, then decrypt successfully with the right password.

## Solution

```powershell
# Create the plaintext file
Set-Content -LiteralPath .\message.txt -Value 'The eagle flies at midnight.'

# Encrypt the file
openssl enc -aes-256-cbc -salt -in .\message.txt -out .\message.enc -pass pass:crypto_is_fun

# Verify the encrypted output is unreadable
Get-Content .\message.enc

# Failed decrypt attempt with the wrong password
openssl enc -d -aes-256-cbc -in .\message.enc -out .\wrong.txt -pass pass:wrong_password

# Successful decrypt attempt with the correct password
openssl enc -d -aes-256-cbc -in .\message.enc -out .\decrypted_message.txt -pass pass:crypto_is_fun

# Confirm the recovered plaintext
Get-Content .\decrypted_message.txt
```

The failed decrypt should produce a `bad decrypt` style error, and the final `Get-Content` should show `The eagle flies at midnight.`
