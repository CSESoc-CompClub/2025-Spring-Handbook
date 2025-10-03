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

## How Does RSA Work? (Simple Version)
1. Pick two prime numbers (For this example we will use 5 and 11)
2. Multiply them together (5 × 11 = 55).
3. Choose a **public exponent** (we will choose 3).
4. Work out a **private exponent** (this is quite difficult to do but in this case, 27 will work).
5. To encrypt: Raise message to the public exponent, then mod by 55.
6. To decrypt: Raise ciphertext to the private exponent, mod by 55.

---

## Practice Task

### Task 1: Encryption
Bob’s RSA public key is **(n = 55, e = 3)**.
Alice wants to send him the number **4**.

👉 Encrypt it (hint: 4³ mod 55).


```html
<input type="text" id="rsa1" />
<button onclick="checkAnswer('rsa1', 'rsa1result', 'OQ==')">Check Answer</button>
<p id="rsa1result" style="display:none;"></p>