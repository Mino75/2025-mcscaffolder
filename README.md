# 🚀 mcscaffolder

A powerful Node.js CLI tool for quickly scaffolding microservice repositories with Docker support, GitHub Actions CI/CD, and Progressive Web App (PWA) capabilities.

## 📋 Table of Contents

- [📖 About](#-about)
- [✨ Features](#-features)
- [🏁 Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [🔨 How to Build](#-how-to-build)
- [▶️ How to Run](#️-how-to-run)
- [📁 Generated Project Structure](#-generated-project-structure)
- [🛠️ Usage](#️-usage)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## 📖 About

mcscaffolder is a microservice scaffolding tool that automates the creation of a complete project structure for building containerized web applications. It generates all the necessary files including Docker configuration, GitHub Actions workflows, Express.js server setup, and PWA manifest files, allowing developers to focus on writing business logic rather than boilerplate code.

The tool is specifically designed to scaffold projects for a game called "Dia" but can be easily modified to scaffold any type of microservice project.

## ✨ Features

- **Express.js Server**: Pre-configured Node.js server with Express framework
- **Docker Support**: Includes optimized Dockerfile using Node.js Alpine image
- **GitHub Actions**: Ready-to-use CI/CD workflow for building and pushing Docker images
- **PWA Ready**: Generates manifest.json and service worker for offline capabilities
- **Zero Configuration**: Creates all necessary files with sensible defaults
- **Lightweight**: Minimal dependencies and fast execution

## 🏁 Getting Started

### Prerequisites

Before using mcscaffolder, ensure you have the following installed:

- Node.js (v14 or higher)
- npm (comes with Node.js)
- Git (for version control)
- Docker (optional, for containerization)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/mcscaffolder.git
cd mcscaffolder
```

2. Make the script executable:
```bash
chmod +x scaffolder.js
```

3. (Optional) Install globally:
```bash
npm install -g .
```

## 🔨 How to Build

Since this is a Node.js script, there's no build process required. However, if you want to package it as an npm module:

1. Ensure your `package.json` includes the bin field:
```json
{
  "name": "mcscaffolder",
  "version": "1.0.0",
  "bin": {
    "mcscaffolder": "./scaffolder.js"
  }
}
```

2. Create an npm package:
```bash
npm pack
```

## ▶️ How to Run

### Method 1: Direct Execution
Navigate to your target directory where you want to create the new project and run:
```bash
node /path/to/scaffolder.js
```

### Method 2: Global Installation
If installed globally:
```bash
mcscaffolder
```

### Method 3: Using npx
```bash
npx /path/to/mcscaffolder
```

## 📁 Generated Project Structure

After running mcscaffolder, you'll get the following structure:

```
your-project/
├── .github/
│   └── workflows/
│       └── main.yml          # GitHub Actions workflow
├── package.json              # Node.js dependencies
├── server.js                 # Express.js server
├── dockerfile                # Docker configuration
├── manifest.json             # PWA manifest
├── service-worker.js         # PWA service worker
├── index.html               # Main HTML file (empty)
├── main.js                  # Main JavaScript file (empty)
├── styles.js                # Styles file (empty)
└── README.md                # Project documentation
```

## 🛠️ Usage

1. **Run the scaffolder** in your desired directory:
```bash
node scaffolder.js
```

2. **Install dependencies** in the generated project:
```bash
npm install
```

3. **Add required assets**:
   - `icon-192.png` - 192x192 PNG icon
   - `icon-512.png` - 512x512 PNG icon
   - `favicon.ico` - Favicon file

4. **Add your content** to:
   - `index.html` - Your HTML content
   - `main.js` - Your JavaScript logic
   - `styles.js` - Your CSS styles

5. **Start the development server**:
```bash
node server.js
```

6. **Build and push Docker image** (requires Docker Hub account):
   - Set up GitHub secrets: `DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN`
   - Manually trigger the GitHub Actions workflow

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2025 Mino

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

Made with ❤️ by Mino
