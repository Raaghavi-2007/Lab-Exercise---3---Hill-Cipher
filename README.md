# Lab-Exercise---3---Hill-Cipher


# Aim:
  To develop a simple C program to implement Hill Cipher.
  
# Procedure:

1. Design of Hill Cipher algorithm using matrix multiplication and modular arithmetic.
2. Implementation using C or python programming.
3. Testing algorithm with different key matrices and plaintext inputs.
4. Apply the Hill Cipher using different key values and verify the corresponding encrypted outputs. 

# Program:
```
key = [[3, 3],
       [2, 5]]

plaintext = input("Enter plaintext: ").upper().replace(" ", "")

# Add X if the plaintext length is odd
if len(plaintext) % 2 != 0:
    plaintext += "X"

ciphertext = ""

for i in range(0, len(plaintext), 2):
    a = ord(plaintext[i]) - ord('A')
    b = ord(plaintext[i + 1]) - ord('A')

    c1 = (3 * a + 3 * b) % 26
    c2 = (2 * a + 5 * b) % 26

    ciphertext += chr(c1 + ord('A'))
    ciphertext += chr(c2 + ord('A'))

print("Plaintext:", plaintext)
print("Ciphertext:", ciphertext)

```

# Output:

<img width="1917" height="217" alt="image" src="https://github.com/user-attachments/assets/a5c9875a-986b-4446-b0d5-8107dafe8721" />

# Result:
The program is executed successfully.
