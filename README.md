# QR CryptoVault

> A lightweight, client-side AES-256-GCM encrypted QR code generator and decryptor.

**Live Web App:** [https://2diworx.github.io/client-side-crypto-qr/](https://2diworx.github.io/client-side-crypto-qr/)

QR CryptoVault lets you store and retrieve sensitive payloads (seed phrases, private keys, backup codes) inside QR codes. All encryption and decryption happen strictly in your browser using standard Web Crypto APIs (`AES-GCM` and `PBKDF2`). No data ever leaves your device or touches a server.

## Features

- **Zero-Knowledge & Air-Gapped**: Runs 100% offline in your browser.
- **Strong Encryption**: Uses AES-GCM (256-bit) with PBKDF2 key derivation (600,000 iterations).
- **Flexible Formats**: Export QR codes as high-resolution PNG or vector SVG.
- **Web Link or Code Only**: Embed a direct decryption link into the QR code or encode just the raw `VAULT:` payload string.
- **Auto-Decrypt via URL**: Accessing a generated web link automatically prompts for the master password to unlock the secret.

## Getting Started

You can use QR CryptoVault directly in your browser or run it locally for maximum air-gapped security:

### Option 1: Web Browser
Access the live deployment directly at [https://2diworx.github.io/client-side-crypto-qr/](https://2diworx.github.io/client-side-crypto-qr/).

### Option 2: Local & Air-Gapped
Since QR CryptoVault is a single self-contained HTML file, running it locally requires no installation:

1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. For air-gapped execution, save the file locally and open it with your network connection turned off.

## Tech Stack

- **HTML5 / CSS3**: Responsive dark-mode interface built with CSS Grid and modern design variables.
- **JavaScript (ES6+)**: Native Web Crypto API (`window.crypto.subtle`).
- **QR Generator**: Powered by [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator).

## Security & Disclaimer

* QR CryptoVault does not send data over network connections or use external telemetry.
* Always ensure your master password is strong and memorable. If you lose your master password, the encrypted data cannot be recovered.

## License

Distributed under the MIT License. See [LICENSE](https://github.com/2diworx/client-side-crypto-qr/blob/main/LICENSE) for more information.
