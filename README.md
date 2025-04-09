# Secure-File-Sharing-Platform---Java-Spring-Boot

A Java Spring Boot-based secure file sharing application that enables encrypted file upload and download using AES encryption and REST APIs. Designed with extensibility in mind for integrating JWT-based authentication and AWS S3 cloud storage.

---

## 🚀 Features

- 🔐 AES encryption for secure file storage
- 📤 Upload and 📥 download endpoints
- 📦 Local encrypted file storage (can be extended to AWS S3)
- ✅ REST API built with Spring Boot
- 🔒 Access control-ready (JWT integration in progress)

---

## 📁 Project Structure

secure-file-sharing/ ├── controller/ │ └── FileController.java ├── service/ │ └── FileService.java ├── util/ │ └── EncryptionUtil.java ├── config/ │ └── SecurityConfig.java └── Application.java

yaml
Copy
Edit

---

## 🛠️ Technologies Used

- Java 11+
- Spring Boot
- Spring Web
- AES Encryption
- (Planned) JWT Authentication
- (Optional) AWS S3 Integration

---

## ⚙️ How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/secure-file-sharing.git
cd secure-file-sharing
2. Build and Run the App
Make sure you have Java 11+ and Maven installed.

bash
Copy
Edit
mvn clean install
mvn spring-boot:run
3. Test the API
🔸 Upload a File
http
Copy
Edit
POST http://localhost:8080/api/files/upload
Body: form-data
Key: file
Value: [Choose a file]

🔸 Download a File
http
Copy
Edit
GET http://localhost:8080/api/files/download/{filename}
Replace {filename} with your uploaded file name (without .enc).

Encrypted files are stored in the encrypted_files/ directory.

🔐 Security
Files are encrypted using AES before storage.

Static AES key is used for demo purposes (in production, store keys securely via environment variables or vaults).

JWT authentication and signed URLs for AWS S3 integration are planned next.

