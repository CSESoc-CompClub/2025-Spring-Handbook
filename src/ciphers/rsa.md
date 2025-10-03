# 🔑 ASYMMETRIC ENCRYPTION & RSA 🔑

## What Makes It *Asymmetric*?

- In **symmetric encryption**, the **same key** is used to both encrypt and decrypt.
  - For instance, in the Ceaser Ciphers covered earlier, we use the same key to encrypt (shift forwards) and decrypt (shift backwards).
- In **asymmetric encryption**, there are **two different keys**:
  - **Public key**: used to lock (encrypt) the message 🔓
  - **Private key**: used to unlock (decrypt) the message 🔑

We call it *asymmetric* since the keys are not the same for encrypting and decrypting.

This means you can safely share your public key with the world,
while keeping your private key secret.


## Why Do We Need RSA?
- Symmetric ciphers (like Substitution or Caesar) need both people to share the **same secret key**.
- But how do we share that key securely over the internet?
- This is a big problem for symmetric encryption schemes.
- RSA solves this by letting you publish your **public key** so anyone can encrypt messages to you.
- Only your **private key** can decrypt it.

---

## How Does RSA Work? (Simplified)
1. Pick two prime numbers (For this example we will use 5 and 11)
2. Multiply them together (n = 5 × 11 = 55).
3. Choose a **public exponent** (we will choose e = 3).
4. Work out a **private exponent** (this is quite difficult to do but in this case, d = 27 will work).
5. We will chose 9, as our message.
6. To encrypt: Raise message to the public exponent, then mod by 55. (9^3 mod 55) = 14
7. To decrypt: Raise ciphertext to the private exponent, mod by 55. (14^27 mod 55) = 9 which was our message!

---

## Practice Task

### Task 1: Encryption
Bob’s RSA public key is n = 55, e = 3.
Alice wants to send him the number **4**.
What will the encrypted message look like (ciphertext)?

**Try to solve before opening the answer!**

<details>
  <summary>Show Answer</summary>

  **Step 1:** formula
  `ciphertext = message^e mod n`

  **Step 2:** plug in numbers
  `ciphertext = 4^3 mod 55`

  **Step 3:** calculate the power
  `4^3 = 64`

  **Step 4:** calculate 64 mod 55
  `64 mod 55 = 9`

  **Encrypted message = 9**

</details>

---

### Task 2: Decryption
Bob’s private key is **d = 27** (with n = 55).
He receives ciphertext **9**.
What is the message, m?
Hint (use this calculator for large values: https://www.wolframalpha.com)

**Try to solve before opening the answer!**

<details>
  <summary>Show Answer</summary>

   **Step 1:** formula
  `message = ciphertext^d mod n`

  **Step 2:** plug in numbers
  `message = 9^27 mod 55`

  **Step 3:** calculate the power (we will need a powerful online calculator like wolfram alpha:
  https://www.wolframalpha.com/input?i=9%5E27)
  `9^27 = 58149737003040059690390169`

  **Step 4:** calculate 58149737003040059690390169 mod 55 (we will also use wolframalpha:
  https://www.wolframalpha.com/input?i=58149737003040059690390169+mod+55)

  `58149737003040059690390169 mod 55 = 4`

  **Decrypted message = 4**

</details>
