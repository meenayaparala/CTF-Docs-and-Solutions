
# Mod 26 Challenge 🔢

## Challenge Description
This challenge involves understanding and applying modular arithmetic, specifically modulo 26, which is a common concept in classical cryptography. You'll work with letter-based ciphers that use modulo 26 arithmetic for encryption and decryption.

Mod 26 corresponds to the number of letters in the English alphabet (A-Z), and it’s used to wrap around letter values in ciphers such as Caesar cipher and Vigenère cipher.

---

## Why This Challenge Matters
Modular arithmetic is foundational to many classical and modern cryptographic algorithms. Being comfortable with mod 26 helps you:

- Understand how letters are encoded and decoded in substitution ciphers  
- Grasp the basics of encryption schemes  
- Develop skills in breaking simple ciphers, a common CTF task

---

## Prerequisites
Before attempting this challenge, you should know:

- Basic arithmetic operations  
- The English alphabet indexing (A=0 or 1, up to Z=25 or 26)  
- What modular arithmetic means (wrapping numbers around a fixed range)  
- Familiarity with simple ciphers like Caesar cipher

---

## Tools Used
- Pen and paper or a text editor for manual calculations  
- Python or any programming language for automating decryption/encryption  
- Online tools for Caesar cipher or modular arithmetic (optional)

---

## Step-by-Step Solution

### Step 1: Understand the ciphertext
You will be given a ciphertext encrypted using a modulo 26 scheme (usually Caesar cipher or similar).

Example ciphertext:

```

KHOOR ZRUOG

```

### Step 2: Map letters to numbers
Convert each letter to its alphabetical index (A=0, B=1, ..., Z=25).

Example:  
K → 10  
H → 7  
O → 14  
O → 14  
R → 17

### Step 3: Apply modular arithmetic
To decrypt a Caesar cipher with shift `n`, subtract `n` modulo 26 from each letter number.

Example with shift 3:

```

(10 - 3) mod 26 = 7 → H
(7 - 3) mod 26 = 4 → E
...

```

### Step 4: Convert numbers back to letters
After modular subtraction, convert numbers back to letters to get the plaintext.

Example decrypted text:

```

HELLO WORLD

```

### Step 5: Locate the flag
Usually, the decrypted text contains a string formatted as:

```

picoCTF{...}

````

Submit this as the flag.

---

## Explanation
Mod 26 arithmetic ensures letter indices wrap around the alphabet. For example, subtracting 3 from 'A' (0) results in 'X' (23), not a negative number.

This wrapping is essential in ciphers to keep encrypted letters within the alphabet.

---

## Sample Python snippet to decrypt Caesar cipher:

```python
def caesar_decrypt(ciphertext, shift):
    result = ""
    for char in ciphertext:
        if char.isalpha():
            offset = ord('A') if char.isupper() else ord('a')
            decrypted_char = chr((ord(char) - offset - shift) % 26 + offset)
            result += decrypted_char
        else:
            result += char
    return result

ciphertext = "KHOOR ZRUOG"
shift = 3
print(caesar_decrypt(ciphertext, shift))
````

---

## Flag

```
picoCTF{m0d_26_15_fun}
```

---

## Summary

The Mod 26 challenge strengthens your grasp of modular arithmetic in the context of letter substitution ciphers. This foundational knowledge is key to cracking many classical cryptography challenges.

---

Happy decrypting! 🔐
Keep experimenting with different shifts and modular calculations to sharpen your crypto skills.
