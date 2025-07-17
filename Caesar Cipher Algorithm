def caesar_encrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            shift_base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - shift_base + shift) % 26 + shift_base)
        else:
            result += char
    return result

def caesar_decrypt(text, shift):
    return caesar_encrypt(text, -shift)

def main():
    last_encrypted_message = None
    last_shift_value = None

    while True:
        print("\n 1. Press E to Encrypt\n 2. Press D to Decrypt\n 3. Type Exit to Exit")
        choice = input("Enter your choice: ").strip().upper()

        if choice == "E":
            message = input("Enter your Message: ")
            try:
                shift = int(input("Please Enter the Shift value: "))
            except ValueError:
                print("Invalid shift. Must be an integer.")
                continue
            encrypted = caesar_encrypt(message, shift)
            last_encrypted_message = encrypted
            last_shift_value = shift
            print(f"Encrypted Message: {encrypted}")

        elif choice == "D":
            if last_encrypted_message is None:
                print("Nothing in the stack to Decrypt.")
            else:
                decrypted = caesar_decrypt(last_encrypted_message, last_shift_value)
                print(f"Decrypted Message: {decrypted}")

        elif choice == "EXIT":
            print("Exiting... All stored messages cleared.")
            break

        else:
            print("Invalid choice. Please select E, D, or Exit.")

if __name__ == "__main__":
    main()
