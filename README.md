# 🚀 Private AI-Assisted Development Server — Raspberry Pi 5

A personal, low-power, remotely accessible AI-assisted development server built using a Raspberry Pi 5.

This project was created as a foundation for developing and experimenting with future AI, automation, software, and hardware projects from a dedicated Raspberry Pi environment.

The server combines Raspberry Pi OS, OpenCode, Git, GitHub, and Tailscale to create a remotely accessible development platform.

---

## 📌 Project Overview

The goal of this project is to transform a Raspberry Pi 5 into a personal development server that can be accessed remotely from a MacBook.

Instead of keeping development projects entirely on a personal computer, the Raspberry Pi acts as the central development environment.

OpenCode provides AI-assisted coding capabilities, Git provides version control, GitHub provides remote project hosting, and Tailscale provides secure remote connectivity.

### Core concept

```text
                 ┌──────────────────┐
                 │      MacBook     │
                 │ Development PC   │
                 └────────┬─────────┘
                          │
                          │ Tailscale
                          │
                 ┌────────▼─────────┐
                 │  Raspberry Pi 5  │
                 │                  │
                 │ Raspberry Pi OS  │
                 │     OpenCode     │
                 │       Git        │
                 └────────┬─────────┘
                          │
                          │ Git
                          ▼
                 ┌──────────────────┐
                 │     GitHub       │
                 │  Project Hosting │
                 └──────────────────┘
```

---

# 🎯 Objectives

The main objectives of this project are:

* Build a personal AI-assisted development server.
* Learn server administration using Raspberry Pi.
* Enable remote development from a MacBook.
* Use AI-assisted programming through OpenCode.
* Learn Git and GitHub-based version control.
* Create a foundation for future AI projects.
* Keep the server accessible remotely without exposing it directly to the public internet.
* Develop a low-power computing platform for experimentation and automation.

---

# 🧰 Hardware

| Component         | Specification    |
| ----------------- | ---------------- |
| Main computer     | Raspberry Pi 5   |
| RAM               | 2 GB             |
| Storage           | 32 GB            |
| Operating system  | Raspberry Pi OS  |
| Primary client    | MacBook          |
| Network           | Wi-Fi / Ethernet |
| Remote networking | Tailscale        |

---

# 💻 Software Stack

### Raspberry Pi OS

Raspberry Pi OS provides the Linux-based operating environment for the server.

### OpenCode

OpenCode is used as the AI-assisted coding environment.

It allows development work to be performed directly within the Raspberry Pi environment.

### Git

Git provides local version control for the project.

It allows changes to be tracked through commits and provides a structured development history.

### GitHub

GitHub is used to host the project's source code and documentation.

This repository is public so the project can be viewed as part of my development portfolio.

### Tailscale

Tailscale provides secure remote networking between the development computer and the Raspberry Pi.

This allows the Raspberry Pi to be accessed remotely without directly exposing the server's SSH service to the public internet.

---

# 🌐 Remote Development Architecture

The Raspberry Pi acts as the server while the MacBook acts as the primary development client.

```text
┌───────────────────────┐
│       MacBook         │
│                       │
│  Terminal / Browser   │
│  Development Client   │
└───────────┬───────────┘
            │
            │ Secure Tailscale Network
            │
┌───────────▼───────────┐
│     Raspberry Pi 5    │
│                       │
│   Raspberry Pi OS     │
│        OpenCode       │
│         Git           │
│     Project Files     │
└───────────┬───────────┘
            │
            │ Git Push / Pull
            │
┌───────────▼───────────┐
│        GitHub         │
│                       │
│ Public Repository     │
│ Source + Documentation│
└───────────────────────┘
```

---

# 🔐 Security Model

The project separates the public project documentation from the private server infrastructure.

### Public

The following can be publicly visible:

* Source code
* Documentation
* Architecture
* Setup instructions
* Project screenshots
* Development information

### Private

The following should never be committed to this repository:

* Passwords
* API keys
* Authentication tokens
* SSH private keys
* Tailscale authentication secrets
* Wi-Fi credentials
* `.env` files containing secrets
* Personal credentials

The Raspberry Pi itself is not intended to be directly exposed to the public internet.

Remote access is performed through the private Tailscale network.

---

# 🛠️ How I Built the Project

## 1. Raspberry Pi Preparation

Started with a Raspberry Pi 5 configured with Raspberry Pi OS.

The Raspberry Pi became the central machine for the project.

### Hardware configuration

```text
Raspberry Pi 5
├── 2 GB RAM
├── 32 GB storage
└── Raspberry Pi OS
```

---

## 2. Network Configuration

The Raspberry Pi was connected to the network and configured for remote access.

Tailscale was then used to establish a private network connection between the Raspberry Pi and development devices.

This allows the Raspberry Pi to remain accessible remotely without requiring direct public exposure.

---

## 3. Remote Access

The Raspberry Pi can be accessed remotely from the MacBook.

The general workflow is:

```text
MacBook
   ↓
Tailscale
   ↓
Raspberry Pi
   ↓
Terminal / Development Environment
```

This makes it possible to work on projects hosted on the Raspberry Pi even when the MacBook and Raspberry Pi are not on the same local network.

---

## 4. OpenCode Installation

OpenCode was installed on the Raspberry Pi as the AI-assisted development environment.

The purpose of this layer is to assist with:

* Code generation
* Code modification
* Project development
* Debugging
* Exploring new software ideas
* Working directly inside the server environment

---

## 5. Git Configuration

Git was configured on the Raspberry Pi to provide local version control.

The basic workflow is:

```bash
git status
git add .
git commit -m "Commit message"
```

Git keeps track of project changes before they are synchronized with GitHub.

---

## 6. GitHub Integration

The Raspberry Pi was authenticated with GitHub and configured to work with GitHub repositories.

The development workflow becomes:

```text
Create / modify project
        ↓
       Git
        ↓
     Commit
        ↓
      Push
        ↓
     GitHub
```

This provides remote backup, version history, and project visibility.

---

# 🔄 Development Workflow

My current workflow is:

```text
1. Connect to Raspberry Pi
              ↓
2. Open project
              ↓
3. Develop with OpenCode
              ↓
4. Test changes
              ↓
5. Track changes with Git
              ↓
6. Commit changes
              ↓
7. Push to GitHub
```

---

# 📂 Recommended Repository Structure

```text
private-ai-server-rpi5/
│
├── README.md
├── .gitignore
│
├── docs/
│   └── setup.md
│
├── scripts/
│   └──
│
└── src/
    └──
```

Additional folders can be added as the project grows.

---

# ⚡ Why Raspberry Pi 5?

The Raspberry Pi 5 provides a compact and low-power Linux computer that can operate as a dedicated development/server platform.

It is particularly useful for:

* Learning Linux
* Server administration
* Remote development
* Automation
* Networking
* Hardware projects
* AI experimentation
* Self-hosted services

The 2 GB model is intended for lightweight development and server workloads rather than large local AI models.

---

# 🧠 AI Architecture

This project should be understood as an **AI-assisted development server**, rather than a high-performance local AI inference server.

The current architecture is:

```text
              AI-Assisted Development
                        │
                        ▼
                    OpenCode
                        │
                        ▼
                Raspberry Pi 5
                        │
             ┌──────────┴──────────┐
             ▼                     ▼
            Git                 Projects
             │
             ▼
          GitHub
```

Future versions can add dedicated local AI inference components.

---

# 🚀 Future Roadmap

## Version 1.0 — Current Foundation

* [x] Raspberry Pi 5 setup
* [x] Raspberry Pi OS
* [x] Remote connectivity
* [x] Tailscale
* [x] OpenCode
* [x] Git
* [x] GitHub integration
* [x] Public project documentation

## Version 2.0 — AI Expansion

* [ ] Local LLM support
* [ ] Ollama
* [ ] AI-powered web interface
* [ ] AI agents
* [ ] Automated project generation
* [ ] Additional AI tools

## Version 3.0 — Infrastructure

* [ ] SSD storage
* [ ] Automated backups
* [ ] Docker
* [ ] CI/CD
* [ ] Monitoring
* [ ] UPS / backup power

## Version 4.0 — Advanced AI Platform

* [ ] AI vision
* [ ] AI automation
* [ ] Hardware integration
* [ ] Multi-service architecture
* [ ] Dedicated AI accelerator

---

# 📊 Project Specifications

| Category              | Current Configuration |
| --------------------- | --------------------- |
| Platform              | Raspberry Pi 5        |
| RAM                   | 2 GB                  |
| Storage               | 32 GB                 |
| OS                    | Raspberry Pi OS       |
| AI Development        | OpenCode              |
| Version Control       | Git                   |
| Cloud Repository      | GitHub                |
| Remote Network        | Tailscale             |
| Primary Client        | MacBook               |
| Repository Visibility | Public                |
| Project Version       | 1.0                   |

---

# 🔒 Privacy Philosophy

The project follows a simple principle:

> **Public code, private infrastructure.**

The source code and documentation can be shared publicly while credentials, private network information, and sensitive configuration remain protected.

---

# 🎓 What This Project Demonstrates

This project demonstrates practical experience with:

* Raspberry Pi administration
* Linux
* Remote networking
* Tailscale
* SSH
* Git
* GitHub
* AI-assisted software development
* Server architecture
* Version control
* Self-hosted development environments

It also provides the foundation for future AI and hardware projects.

---

# 🚀 Future Vision

This Raspberry Pi 5 server is intended to become the central development platform for future personal projects.

The long-term goal is to evolve the system from a simple AI-assisted development server into a broader personal AI and automation platform.

---

## 👨‍💻 Project

**Private AI-Assisted Development Server**

**Platform:** Raspberry Pi 5

**Status:** Active Development

**Version:** 1.0

---

⭐ If you find this project interesting, feel free to explore the repository and follow its development.
