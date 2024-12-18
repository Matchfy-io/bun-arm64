# Bun Docker Image for ARM64

Welcome to the **Bun Docker Image for ARM64** project! This repository provides a pre-built Docker image for running the [Bun JavaScript runtime](https://bun.sh/) on ARM64 architecture, enabling development and production use on platforms like Raspberry Pi, Apple M Series, and other ARM64-based systems.

---

<br/>

## 🚀 **Features**

- 🛠️ **Lightweight**: Optimized for ARM64 architecture.
- ⚡ **Fast**: Leverages Bun's speed and performance benefits.
- 📦 **Ready-to-use**: Pre-built and easy to pull from Docker Hub.
- 🔧 **Customizable**: Simple to extend and modify.

---

## 📋 **Prerequisites**

Before you start, make sure you have the following installed:

- **Docker** (20.10 or later)
- **ARM64-based system** (e.g., Raspberry Pi, Apple M1/M2, AWS Graviton)

To verify your system architecture, you can run:

```bash
uname -m
```

You should see `aarch64` or similar for ARM64.

---

## 📦 **Getting Started**

Follow the steps below to get started with this Docker image.

### 1️⃣ **Pull the Image**

You can pull the latest version of the Bun ARM64 Docker image from Docker Hub:

```bash
docker pull matchfyio/bun-arm64:latest
```

### 2️⃣ **Run the Container**

To run the container, use the following command:

```bash
docker run --rm -it matchfyio/bun-arm64:latest bun --version
```

This will display the Bun version and confirm that the image is working correctly.

### 3️⃣ **Run a Bun Script**

To run a Bun script, you can mount a local directory to the container:

```bash
docker run --rm -it -v $(pwd):/app -w /app matchfyio/bun-arm64:latest bun run myscript.js
```

This command mounts your current working directory to `/app` inside the container, making it easy to test and run scripts.

---

## ⚙️ **Build the Image (Optional)**

If you want to build the Docker image yourself, you can do so with the following command:

```bash
git clone https://github.com/Matchfy-io/bun-arm64.git
cd bun-docker-arm64
docker build -t matchfyio/bun-arm64:latest .
```

This will build the image locally and tag it as `matchfyio/bun-arm64:latest`.

---

## 📂 **Project Structure**

```
├── Dockerfile          # Dockerfile defining the Bun ARM64 image
├── README.md           # Project documentation (this file)
```

---

## 🙌 **Contributing**

Contributions, issues, and feature requests are welcome! Feel free to check out the [issues page](https://github.com/Matchfy-io/bun-arm64/issues) if you want to contribute.

### **How to Contribute**

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature-name`.
3. Make your changes and commit them: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature/your-feature-name`.
5. Open a pull request.
