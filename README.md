def caesar_cipher(text, shift):
    result = ''
    for char in text:
        if char.isalpha():
            shifted_char = chr(((ord(char) - 65 + shift) % 26) + 65) if char.isupper() else chr(((ord(char) - 97 + shift) % 26) + 97)
            result += shifted_char
        else:
            result += char
    return result

# Example usage:
text = "Hello, World!"
shift = 3
encrypted_text = caesar_cipher(text, shift)
print("Encrypted:", encrypted_text)
decrypted_text = caesar_cipher(encrypted_text, -shift)  # Decrypt by shifting back
print("Decrypted:", decrypted_text)
