# QR Code Generator - Assignment 7

This application generates QR codes using Docker.

## Links

### GitHub Repository
![GitHub QR Code](qr_codes/QRCode_20251004213502.png)

### DockerHub Image  
![DockerHub QR Code](qr_codes/QRCode_20251004213503.png)

## How to Run

Pull from DockerHub:
```bash
docker pull pruthul123/qr-code-generator
docker run -v $(pwd)/qr_codes:/app/qr_codes pruthul123/qr-code-generator