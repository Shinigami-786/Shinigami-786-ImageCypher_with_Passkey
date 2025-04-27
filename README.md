# 📸🔐 imageCypher

A secure image encryption and decryption tool built with **Node.js** and **React**.  
It uses **XOR cipher encryption** with randomly generated keys and verifies key integrity using **SHA-256 hash verification**.  
Designed to safely share images over potentially insecure platforms like WhatsApp or cloud storage.

---

## 📌 Features

- 📷 Encrypt images using XOR cipher
- 🔑 Generate Base64-encoded encryption keys
- 📝 Generate and store SHA-256 hash for key verification
- 🖥️ Drag-and-drop user interface
- 🌙 Dark mode toggle support
- 📦 Automatic download of encrypted image, key, and hash as ZIP
- ✅ Key hash verification before decryption
- 🧹 Secure cleanup by deleting hash file after decryption

---

## 📽️ Why imageCypher?

While messaging apps like WhatsApp offer end-to-end encryption for messages and images during transit, once files are downloaded to a device or shared via other platforms, their security can be compromised.

### imageCypher ensures:

- The image is securely encrypted before sending.
- Only the intended recipient with the correct key can decrypt it.
- The integrity of the key is verified before decryption using a SHA-256 hash.
- No residual hash files are left after decryption.

---

## 📂 Project Structure

/backend ├── encrypt.js └── decrypt.js

/frontend └── src/ ├── components/ └── App.js └── styles/

/uploads └── (encrypted images, keys, hashes)

README.md package.json

---

## ⚙️ How it Works

### Encryption

- Upload an image.
- A random key (same size as image data) is generated.
- Image is encrypted with XOR cipher.
- Key is Base64-encoded and saved.
- SHA-256 hash of key is generated and saved.

### Decryption

- Encrypted image and key are uploaded.
- SHA-256 hash is recomputed from the key.
- Hash is compared with the stored hash.
- If matched, image is decrypted.
- Hash file is deleted after successful decryption.

---

## 📦 Installation

Follow the steps below to set up and run `imageCypher` locally:

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/imageCypher.git
   cd imageCypher
   ```

2. Install backend dependencies
   ```bash
   cd backend
   npm install
   ```
   
3. Install frontend dependencies
   ```bash
   cd ../frontend
   npm install
   ```

---

## 🚀 Usage

- Start backend server.
- Start frontend React app.
- Use drag-and-drop UI to encrypt or decrypt images.
- Download encrypted files, key, and hash as ZIP.
- Share encrypted image and key separately.

---

## 🛡️ Security Note

This tool provides **application-level encryption and integrity checking**.  
While XOR cipher is simple, combining it with proper key management and hash verification significantly improves the safety of image sharing.

---

## ⭐️ Support

If you like this project, give it a ⭐️ and consider contributing!




