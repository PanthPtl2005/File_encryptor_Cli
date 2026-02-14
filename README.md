# Lock Forge

A lightweight CLI tool to securely encrypt and decrypt local files using strong AES-256 encryption. Built with Bash and OpenSSL, designed to be simple, fast, and usable directly from the terminal.

---

## Overview

Lock Forge protects sensitive files by encrypting them with industry-standard cryptography. It uses OpenSSL’s AES-256 in **GCM mode** with PBKDF2 key derivation to ensure strong password-based security and built-in integrity verification.

---

## Features

- AES-256 encryption using OpenSSL (GCM mode)  
- Authenticated encryption (confidentiality + integrity)  
- Password-based key derivation (PBKDF2)  
- File encryption and decryption  
- Hidden password input  
- Wrong password / tampering detection  
- Lightweight and dependency-minimal  

---

## Requirements

### Operating System
Lock Forge is designed for Unix-like environments:
- macOS 
- Linux (Ubuntu, Debian, Arch, Kali, Fedora)  

Windows users can run the tool using:
- WSL (Windows Subsystem for Linux)  
- Git Bash (limited support)  

Bash Shell
- Bash version 4 or higher is recommended.

Check Bash version:
```bash
bash --version
```

OpenSSL Version
```bash
openssl version
```
Install if missing:
macOS (Homebrew)
```bash
brew install openssl
```
Ubuntu\Debain
```bash
sudo apt install openssl
```
Arch Linux
```bash
sudo pacman -S openssl
```
Fedora
```bash
sudo dnf install openssl
```
### Installation
Clone the repository
```bash
git clone https://github.com/PanthPtl2005/File_encryptor_Cli-aka-LockForge.git
```

Permissions
```bash
chmod +x file_encryptor.sh
```

Run
```bash
./File_encryptor.sh
```
### Encryption Details
- Algorithm: AES-256-GCM
- Key Derivation: PBKDF2
- Salt: Automatically generated and stored with file
- Integrity: Built-in authentication tag (tamper detection)

### Security Notes
- Losing the password means permanent data loss
- Passwords are never stored anywhere
- Salt, IV, and authentication tag are stored inside the encrypted file
- Decryption fails automatically if:
- Wrong password is used
- File is modified or corrupted



