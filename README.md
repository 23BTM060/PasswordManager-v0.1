# 🔐 GUI Password Manager – INS Course Project

A GUI-based password manager designed to securely store and retrieve credentials. This project is developed step-by-step to demonstrate key concepts from the **Information and Network Security (INS)** syllabus, including encryption algorithms, access control, secure storage, and key management.

---

## 🧩 Project Stages (Aligned with Syllabus)

---

### ✅ Stage 1: GUI-Based Password Storage with AES (Unit-II)

- **Topic(s)**: AES, Symmetric Encryption
- **Goal**: Implement AES-based encryption and decryption using a hardcoded key.
- **Features**:
  - GUI to add, view, and delete passwords
  - All credentials stored in encrypted format
  - AES-128 or AES-256 using Python's `cryptography` library

---

### ✅ Stage 2: Algorithm Selection – AES and RSA (Unit-II)

- **Topic(s)**: AES, RSA, Symmetric vs Asymmetric
- **Goal**: Allow user to select between AES (symmetric) and RSA (asymmetric).
- **Features**:
  - AES for fast local encryption
  - RSA for demonstration of key pair encryption
  - Option in GUI to choose algorithm
  - Hardcoded or internally generated RSA key pair

---

### ✅ Stage 3: Secure Master Password & Access Control (Unit-III)

- **Topic(s)**: Access Control, Security Policies
- **Goal**: Restrict access using a secure login system.
- **Features**:
  - Master password required to access vault
  - Master password is hashed and stored securely
  - Lockout after N incorrect attempts (configurable)
  - Optional: Show password strength meter

---

### ✅ Stage 4: Export & Import Encrypted Password Vault (Unit-III)

- **Topic(s)**: File Security, Data Handling
- **Goal**: Enable backup and restoration of encrypted data.
- **Features**:
  - Export all data to `.vault` or `.encjson` file
  - Encrypted file is useless without correct key
  - Import feature with algorithm match check

---

### ✅ Stage 5: Key Management and Random Key Generation (Unit-II & IV)

- **Topic(s)**: Key Generation, CRT, PRNG, Key Management
- **Goal**: Implement secure key generation and storage.
- **Features**:
  - Generate AES keys using cryptographically secure PRNG
  - GUI for generating and rotating keys
  - Secure key handling (keys not stored in plaintext)
  - Optionally store RSA private/public keys securely

---

### ✅ Stage 6: Secure Transport with HTTPS for Remote Sync (Unit-IV)

- **Topic(s)**: TLS, HTTPS, SSH, Secure Channels
- **Goal**: (Optional/Bonus) Export password vault to remote location using HTTPS.
- **Features**:
  - Use HTTPS POST to upload encrypted file to remote server (simulated or localhost)
  - Ensure TLS/SSL channel is verified
  - Demo use of HTTPS with self-signed certificate

---

### ✅ Stage 7: VPN/PGP-Themed UI Options (Unit-V – Optional UI Flavor)

- **Topic(s)**: VPNs, PGP, IPsec
- **Goal**: Add design/UX flavor to simulate VPN/PGP-style environment.
- **Features**:
  - Display "PGP-style" identity key in UI
  - Optional IPsec/Pseudonym login messages
  - **No real VPN or PGP implementation**

---

## 🖥️ Tech Stack

- **Python 3.11+**
- **Tkinter / ttkbootstrap** for GUI
- **Cryptography** (`Fernet`, `AES`, `RSA`)
- **hashlib** for password hashing
- **json / csv** for data export

---

## 🧠 INS Topics Covered

| Syllabus Unit | Concepts Used in Project |
|---------------|--------------------------|
| Unit I | Overview of security concepts |
| Unit II | AES, RSA, PRNG, CRT, Symmetric/Asymmetric |
| Unit III | Access Control, IDS-style validation |
| Unit IV | SSL/TLS (for file export over HTTPS), Key Management |
| Unit V | PGP-like UI references, VPN theme (optional visuals only) |

---

## 📁 Folder Structure (Example)

```bash
PasswordManager/
├── main.py
├── encryption/
│   ├── aes_handler.py
│   ├── rsa_handler.py
├── gui/
│   ├── login.py
│   ├── dashboard.py
├── data/
│   ├── vault.encjson
├── keys/
│   ├── aes.key
│   ├── rsa_private.pem
│   ├── rsa_public.pem
├── README.md
└── requirements.txt
