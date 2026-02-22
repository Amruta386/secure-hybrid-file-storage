🔐 Secure Hybrid Encrypted File Storage System
Overview
The Secure Hybrid Encrypted File Storage System is a multi-layered cryptographic solution designed to provide high-level confidentiality, integrity, and controlled access for digital file storage.
This system combines symmetric encryption (AES-256), asymmetric key protection (RSA-2048), chaos-based cipher diffusion, compression techniques, and OTP-based verification to create a secure and efficient file management platform.
The project demonstrates practical implementation of hybrid encryption architecture in a real-world web application environment.

Objectives

Implement a high-performance hybrid encryption model
Ensure secure key management using asymmetric cryptography
Add an additional non-linear security layer using chaos theory
Provide authenticated access with OTP verification
Maintain data integrity through cryptographic hashing
Deliver a clean, structured, and user-friendly interface

System Architecture
The platform follows a structured encryption and decryption pipeline:

Encryption Workflow

User authentication and session validation
File upload and preprocessing
Optional compression
AES-256 symmetric encryption
RSA-2048 public key wrapping of AES key
Chaos-based ciphertext transformation
Metadata generation and secure storage

Decryption Workflow

OTP verification
RSA private key unwrapping
Reverse chaotic diffusion
AES-256 decryption
File restoration and secure download

Core Modules

Authentication & Session Management

Secure user registration and login
Password hashing
Session protection using Flask-Login
User-isolated storage directories

File Processing Engine

Supports multiple file formats
Binary conversion and preprocessing
File size and metadata extraction

AES Encryption Module
256-bit symmetric encryption
Random key and IV generation
High-speed encryption for large files

RSA Key Management

2048-bit asymmetric encryption
Secure AES key wrapping
Prevents unauthorized key access

Chaos-Based Security Layer

Logistic map-based diffusion
Enhances randomness
Reduces statistical attack feasibility

Compression Module

ZIP-based storage optimization
Tracks compression statistics

Metadata & Audit Logging

Stores IV, wrapped key, hash, timestamps
SHA-256 integrity verification

Ensures traceability

OTP-Based Access Control

Email-based one-time password verification
Two-factor protection before decryption

Technology Stack
Backend
 Python
 Flask
 Flask-Login

Cryptography & Security
 PyCryptodome
 AES-256
 RSA-2048
 SHA-256

Data Handling
 JSON Metadata
 ZIP Compression

Security Design Highlights

Hybrid encryption for balanced performance and security
Separation of encryption and key management
Multi-layer defense model (AES + RSA + Chaos + OTP)
Integrity validation using SHA-256 hashing
Encrypted-only storage policy
User-isolated file environments

Performance & Testing

Successfully tested with documents, images, and media files
Verified encryption and decryption consistency
Confirmed decryption failure with incorrect keys
Demonstrated secure OTP validation mechanism
Observed expected ciphertext size variation due to encryption randomness

Installation
git clone https://github.com/your-username/secure-hybrid-encrypted-storage.git
cd secure-hybrid-encrypted-storage
pip install -r requirements.txt
python app.py

Usage

Register a new user account
Login securely
Upload a file
Encrypt and store
Request OTP for decryption
Download restored file

Future Enhancements

Cloud storage integration (AWS / Azure / GCP)
Hardware Security Module (HSM) support
Secure file sharing between users
API integration for enterprise deployment
Advanced audit logging and monitoring
