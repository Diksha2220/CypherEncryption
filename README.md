<div align="center">
    <img src="https://github.com/Diksha2220/Media/blob/main/GreenCypher.png" alt="Description of Image" width="500"/>
</div>

## 🔐 Caesar Cipher Encryption & Decryption

### 📜 Summary
This project implements a simple Caesar cipher for encrypting and decrypting text. The Caesar cipher shifts each letter by a specified number of places in the alphabet, wrapping around if necessary. Non-alphabetic characters remain unchanged.

### 🛠️ Functions

- **`caesar_cipher_encrypt(plaintext, shift)`**: Encrypts the given plaintext using the specified shift.
- **`caesar_cipher_decrypt(encrypted_text, shift)`**: Decrypts the given encrypted text by reversing the shift.

### 🚀 How It Works

1. **Encryption**:
   - Shifts each alphabetic character in the plaintext by the shift value.
   - Preserves the case of the letters.
   - Leaves non-alphabetic characters unchanged.

2. **Decryption**:
   - Reverses the shift applied during encryption to restore the original text.

### 🔧 Usage

```python
def caesar_cipher_encrypt(plaintext, shift):
    encrypted_text = ""
    for char in plaintext:
        if char.isalpha():
            shift_amount = shift % 26
            if char.islower():
                new_char = chr((ord(char) - ord('a') + shift_amount) % 26 + ord('a'))
            else:
                new_char = chr((ord(char) - ord('A') + shift_amount) % 26 + ord('A'))
            encrypted_text += new_char
        else:
            encrypted_text += char
    return encrypted_text

def caesar_cipher_decrypt(encrypted_text, shift):
    return caesar_cipher_encrypt(encrypted_text, -shift)

def main():
    text_to_encrypt = input("Enter the text to encrypt: ")
    shift = int(input("Enter the shift value (an integer): "))
    encrypted_text = caesar_cipher_encrypt(text_to_encrypt, shift)
    print("Encrypted text:", encrypted_text)
    decrypted_text = caesar_cipher_decrypt(encrypted_text, shift)
    print("Decrypted text:", decrypted_text)

if __name__ == "__main__":
    main()
```

### 📝 Example

```plaintext
Enter the text to encrypt: Hello, World!
Enter the shift value (an integer): 3
Encrypted text: Khoor, Zruog!
Decrypted text: Hello, World!
```
📄 [View Main Code File](https://github.com/Diksha2220/CypherEncryption/blob/main/CypherMainCode.txt)
---
<div align="center">
    <img src="https://github.com/Diksha2220/Media/blob/main/lockKey.gif" alt="Description of Image" width="500"/>
</div>


