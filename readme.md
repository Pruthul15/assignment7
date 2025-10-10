# QR Code Generator - Assignment 7

A Dockerized Python application that generates QR codes for any URL.

## Description
This application generates QR codes using Docker containerization. It demonstrates modern deployment practices including Docker images, volume mounts, and automated CI/CD with GitHub Actions.

## Features
- Generates QR codes with customizable colors
- Dockerized for easy deployment and portability
- Automated CI/CD pipeline with GitHub Actions
- Volume mounts for persistent storage
- Security best practices (non-root user)

## Links

### GitHub Repository
Scan this QR code to visit the GitHub repository:

![GitHub QR Code](qr_codes/QRCode_20251004213502.png)

### DockerHub Image  
Scan this QR code to visit the DockerHub image:

![DockerHub QR Code](qr_codes/QRCode_20251004213503.png)

**Direct Links:**
- GitHub: https://github.com/Pruthul15/assignment7
- DockerHub: https://hub.docker.com/r/pruthul123/qr-code-generator

## How to Run

### Option 1: Pull from DockerHub
```bash
# Pull the image
docker pull pruthul123/qr-code-generator

# Run with default URL
docker run -v $(pwd)/qr_codes:/app/qr_codes pruthul123/qr-code-generator

# Run with custom URL
docker run -v $(pwd)/qr_codes:/app/qr_codes pruthul123/qr-code-generator --url https://example.com
```

### Option 2: Build Locally
```bash
# Clone the repository
git clone https://github.com/Pruthul15/assignment7.git
cd assignment7

# Build the Docker image
docker build -t pruthul123/qr-code-generator .

# Run the container
docker run -v $(pwd)/qr_codes:/app/qr_codes pruthul123/qr-code-generator
```

## Project Structure
```
assignment7/
├── .github/
│   └── workflows/
│       └── docker.yml          # GitHub Actions workflow
├── qr_codes/                   # Generated QR codes (not tracked in git)
├── Dockerfile                  # Docker image definition
├── docker-compose.yml          # Docker Compose configuration
├── main.py                     # QR code generator application
├── requirements.txt            # Python dependencies
├── .dockerignore              # Docker ignore rules
├── .gitignore                 # Git ignore rules
└── readme.md                  # This file
```

## Requirements
- Docker Desktop (Windows/Mac) or Docker Engine (Linux)
- WSL 2 (for Windows users)
- Git

## Technical Details

### Docker Configuration
- Base Image: `python:3.12-slim-bullseye`
- Non-root user: `myuser`
- Volume mount: `/app/qr_codes`
- Port: Not required (CLI application)

### CI/CD Pipeline
GitHub Actions automatically:
1. Builds the Docker image on every push to main
2. Logs into DockerHub
3. Pushes the image to DockerHub with `latest` tag

## Assignment Information
- **Course:** IS601 - Python for Web API Development
- **Module:** Module 7 - Docker and Containerization
- **Instructor:** Professor Licciardello
- **Semester:** Fall 2025

## License
This project is for educational purposes as part of NJIT coursework.

---

**Author:** Pruthul Patel  
**Course:** IS 601 - Module 7 Assignment