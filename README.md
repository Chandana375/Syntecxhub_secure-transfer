 🔐 Secure File Transfer & Encrypted Storage System

 📌 Overview

This project implements a secure file transfer system that ensures confidentiality, integrity, and secure storage of files using modern cryptographic techniques.

It simulates an industry-level secure cloud storage system with features similar to Amazon S3, Google Drive, and Dropbox.



🚀 Features

* AES-256 Encryption – Encrypt files before transmission
* HMAC Integrity Verification – Detect tampering
* JWT Authentication – Secure API access
* Chunked File Upload – Efficient handling of large files
* Resume Upload Support – Avoid re-uploading existing chunks
* SHA-256 File Hashing – Additional integrity verification
* Malware Detection (Simulation) – Blocks suspicious uploads
* Security Logging – Tracks system activity
* SOC Monitoring Dashboard – View security events
* HTTPS Support (Optional) – Prevent MITM attacks
* Encrypted Storage – Files stored securely on server



 🏗 Project Structure

secure_transfer_enterprise_final/

server/
    server.py
    server.log

client/
    crypto_utils.py
    upload_client.py
    download_client.py
    test.txt

storage/
    encrypted.bin
    chunks/
 ⚙️ Installation


 1. Clone Repository

git clone <your-repo-url>
cd secure_transfer_enterprise_final


 2. Install Dependencies

pip install flask cryptography requests pyjwt


 ▶️ Usage

 Step 1: Start Server

cd server
python server.py

Step 2: Upload File

Open a new terminal:

cd client
echo "Hello Secure World" > test.txt
python upload_client.py

 Step 3: Download File

python download_client.py

 📊 SOC Dashboard

View system activity:

http://127.0.0.1:5000/soc_dashboard


 🔐 Security Architecture

Client
  │
  │ AES Encryption + HMAC
  │
  ▼
HTTPS Secure Channel
  ▼
Secure Server
  │
  ├── JWT Authentication
  ├── Chunk Upload
  ├── Malware Detection
  ├── Logging
  │
  ▼
Encrypted Storage


 ⚠️ Threat Model & Mitigation

Man-in-the-Middle (MITM)
Mitigation: HTTPS, encryption before transfer

Data Tampering
Mitigation: HMAC verification, SHA-256 hashing

Unauthorized Access
Mitigation: JWT authentication

Malware Upload
Mitigation: server-side scanning

Data Loss or Corruption
Mitigation: chunked upload with resume support



🛠 Technologies Used

Python
Flask
Cryptography (AES-GCM)
HMAC (SHA-256)
JWT Authentication
REST API


📌 Future Enhancements

Real malware scanning (ClamAV)
Role-based authentication
Web dashboard UI
Cloud deployment (AWS / Azure)
Key management system (KMS)

