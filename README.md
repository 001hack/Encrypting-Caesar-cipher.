# encrypting-Caesar-cipher.
Creating Python script that encrypts a given text using the Caesar cipher.

def caesar_cipher_encrypt(text, shift):
    encrypted_text = ""

    for char in text:
        # Check if the character is an uppercase letter
        if char.isupper():
            encrypted_text += chr((ord(char) + shift - 65) % 26 + 65)
        # Check if the character is a lowercase letter
        elif char.islower():
            encrypted_text += chr((ord(char) + shift - 97) % 26 + 97)
        # If it's neither, leave it as it is (e.g., punctuation or space)
        else:
            encrypted_text += char

    return encrypted_text
if name == "main":

    # Input text from user
    text = input("Enter the text to encrypt: ")

    # Input shift value from user
    shift = int(input("Enter the shift value (number): "))

    # Call the encryption function
    encrypted_text = caesar_cipher_encrypt(text, shift)

    # Display the encrypted text
    print("Encrypted Text:", encrypted_text)
