# AroSaina 🔒
Note: This is a private, proprietary software. All rights reserved.

**AroSaina** is a secure, serverless peer-to-peer file transfer application built with Flutter. It enables direct, encrypted file sharing between devices using Wi-Fi Direct technology. Operating completely offline without central servers or internet connectivity, AroSaina delivers a private, secure, and intuitive local file sharing experience where your data never leaves your control.
## 🚀 Core Features

### 🔒 **Security-First Architecture**
- **End-to-End Encryption**: Implements AES-GCM 256-bit encryption for all file transfers, ensuring military-grade protection of your data in transit
- **Secure Session Management**: Cryptographic session keys securely managed using `cryptography` and `flutter_secure_storage` packages
- **Zero Data Leakage**: No files pass through third-party servers; all transfers occur directly between devices
- **Transfert Controll**: Set how many times a files can be transfered
### 📡 **Advanced P2P Technology**
- **Wi-Fi Direct Connectivity**: Utilizes the `nearby_connections` package for establishing direct device-to-device connections
- **Offline Operation**: Complete functionality without internet access - perfect for remote areas or secure environments
- **High-Speed Transfers**: Leverages local network speeds for rapid file sharing

### 🎯 **Smart Transfer Management**
- **QR Code Pairing**: Simple one-scan connection setup that securely transmits session details
- **Digital Rights Management**: Custom DRM mechanism controlling file redistribution limits
- **Transfer History**: Local storage of transfer metadata using Hive for efficient data management
- **Batch Operations**: Support for multiple file transfers in single sessions

## 🛠️ Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Framework** | Flutter 3.x | Cross-platform UI development |
| **State Management** | flutter_bloc 8.x | Predictable state management |
| **P2P Connectivity** | nearby_connections | Wi-Fi Direct device communication |
| **Encryption** | cryptography | AES-GCM 256-bit encryption |
| **Secure Storage** | flutter_secure_storage | Secure key management |
| **Local Database** | Hive | Efficient local data persistence |
| **QR Generation** | qr_flutter | QR code creation and display |
| **QR Scanning** | mobile_scanner | QR code scanning capabilities |
| **Dependency Injection** | get_it | Service location and DI |
| **Logging** | logger | Structured application logging |

## 🔐 Security Implementation Details

### Encryption Flow
1. **Session Establishment**: Devices exchange public keys via QR codes
2. **Key Derivation**: Shared secret derived using ECDH key exchange
3. **Symmetric Encryption**: AES-GCM 256-bit keys generated for each session
4. **File Encryption**: Files encrypted in chunks with authentication tags
5. **Verification**: Integrity verified using GCM authentication tags

### Permission Model
- **Storage Access**: Required for file selection and saving
- **Location Services**: Required for Wi-Fi Direct discovery (Android)
- **Camera Access**: Required for QR code scanning
- **Wi-Fi Management**: Required for establishing P2P connections

## 📱 Usage Guide

### Sending Files
1. Launch AroSaina on both sending and receiving devices
2. On sending device, tap "Send" and select files
3. Generate QR code for the session
4. On receiving device, tap "Receive" and scan the QR code
5. Accept connection request on both devices
6. Monitor transfer progress in real-time

### Receiving Files
1. Open AroSaina and select "Receive" mode
2. Scan the sender's QR code
3. Review file details and accept transfer
4. Encrypted files are automatically decrypted and saved
5. Check transfer history for received files

## 📄 License

This project is proprietary software. All rights reserved.

## 🆘 Support

For technical issues or security concerns:
1. Check the troubleshooting section below
2. Review application logs
3. Ensure devices support Wi-Fi Direct
4. Verify sufficient storage space

### Common Issues
- **Connection Failed**: Ensure devices are within range (typically < 30m)
- **Slow Transfers**: Move devices closer together for better signal
- **QR Code Not Scanning**: Ensure adequate lighting and camera focus
- **Permission Denied**: Grant all required permissions in device settings

## 🏢 Enterprise Considerations

AroSaina is suitable for:
- **Government Agencies**: Secure document transfer without cloud dependencies
- **Healthcare**: HIPAA-compliant medical record sharing
- **Legal Firms**: Confidential document exchange
- **Education**: Offline resource sharing in low-connectivity areas
- **Military**: Secure communications in field operations

---

**Disclaimer**: AroSaina is designed for legitimate file sharing purposes. Users are responsible for complying with all applicable laws and regulations regarding file sharing and data transfer in their jurisdiction.

*Last Updated: 10 december 2025
