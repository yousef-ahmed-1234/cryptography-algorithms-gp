# Cryptography Project Suite

This repository contains a comprehensive cryptography project implemented in **PARI/GP**, demonstrating secure key exchange, encryption/decryption, digital signatures, and threshold signatures. The project uses a personal image hash as the base message for all cryptographic operations.

---

## **Project Overview**

The project consists of **four main scripts**, each covering a different cryptographic primitive:

1. **Diffie-Hellman Key Exchange (`dh.gp`)**
   - Generates a safe prime `p` and generator `g`.
   - Simulates two parties exchanging keys to derive a shared secret.
   - Computes a symmetric key from the hash integer modulo `p`.
   - **Key outputs:**
     - Shared secret (A & B)
     - Symmetric key derived from `m mod p`

2. **ElGamal Encryption & Signatures (`elgamal.gp`)**
   - Performs ElGamal encryption and decryption over a large finite field.
   - Generates digital signatures `(r, s)` and verifies them.
   - **Key outputs:**
     - Public key
     - Ciphertext `(c1, c2)`
     - Decrypted message `M'`
     - Signature and verification result

3. **Elliptic Curve ElGamal (ECDSA) (`elgamalec.gp`)**
   - Maps the hash integer to an elliptic curve point.
   - Generates a private key `d` and public key `Q`.
   - Performs EC encryption and creates an ECDSA signature.
   - **Key outputs:**
     - Public and private keys
     - Encrypted points `(C1, C2)`
     - Signature `(r, s)` and verification result

4. **Pedersen Threshold Signature (`pedestrianthreshold.gp`)**
   - Implements a threshold signature scheme with multiple players.
   - Secret polynomial is distributed as shares.
   - Aggregates partial signatures to verify the threshold signature.
   - **Key outputs:**
     - Player shares `s1, s2, s3`
     - Final threshold signature `(H(m), S)`
     - Verification result

---

## **Project Features**

- **Secure Key Exchange:** Diffie-Hellman ensures both parties arrive at the same secret.
- **Encryption & Digital Signatures:** ElGamal provides confidentiality and authenticity.
- **Elliptic Curve Cryptography:** Strong security for smaller key sizes using ECDSA.
- **Threshold Signatures:** Pedersen scheme enables distributed trust and multi-party signing.
- **Consistent Input:** All scripts use the same message derived from a SHA-256 hash of an image.

---


