
# Draw It or Lose It – Software Design Document

## 📌 Project Overview

**Draw It or Lose It** is a cross-platform multiplayer game originally developed for Android. The Gaming Room has requested a redesign of the game architecture to expand support for web, desktop, and mobile platforms. This project presents a software design solution using scalable and secure system architecture with a focus on Linux-based distributed systems, modular code, and real-time synchronization.

## 📚 Document Details

- **Course**: CS 230 - Software Design and Engineering  
- **Institution**: Southern New Hampshire University  
- **Project**: Software Design Template  
- **Application**: Draw It or Lose It  
- **Version**: 1.0  
- **Author**: Adil Patel  
- **Submission Date**: June 24, 2025  

## 📄 Table of Contents

- Executive Summary  
- Requirements  
- Design Constraints  
- System Architecture View  
- Domain Model  
- Evaluation  
- Recommendations  
- Document Revision History  

## 🧾 Executive Summary

The Gaming Room seeks to scale "Draw It or Lose It" for broader reach across platforms. This document outlines a Linux-based solution emphasizing real-time interaction, security, and reliability. It addresses development constraints, distributed architecture, and tools required to ensure seamless multi-platform gameplay.

## ✅ Requirements

- Cross-platform support (web, desktop, mobile)  
- Real-time multiplayer functionality  
- Secure user data handling  
- Cloud service integration  
- High availability and scalability  

## 🚧 Design Constraints

- Real-time, low-latency network communication  
- Platform compatibility (web, desktop, mobile)  
- Device resource limitations  
- Data synchronization across distributed instances  
- Security and data protection compliance  

## 🧱 Domain Model

The domain model includes:
- **GameRoom** – Manages sessions and player registration  
- **Player** – Holds user data and gameplay interaction  
- **GameSession** – Controls the game lifecycle and flow  

Principles applied: Object-oriented design (inheritance, encapsulation), and design patterns (Singleton, Iterator).

## 🖥️ Evaluation Table

| Development Requirements | Mac | Linux | Windows | Mobile Devices |
|--------------------------|-----|--------|---------|----------------|
| **Server Side** | Limited production use; lacks enterprise support. | Ideal for distributed, scalable systems; highly compatible. | Enterprise-ready but less flexible; higher cost. | Not suitable for hosting. |
| **Client Side** | Requires macOS-specific builds; premium user base. | Focus on web compatibility; niche desktop usage. | Largest user base; testing is critical. | Dual development for Android and iOS needed. |
| **Development Tools** | Xcode, IntelliJ, VS Code; supports Swift, Java. | Eclipse, IntelliJ, VS Code; supports Java, Python, C++. | Visual Studio, IntelliJ, WSL; great Windows support. | Android Studio, Xcode, Flutter, React Native. |

## 💡 Recommendations

### 1. **Operating Platform**  
**Ubuntu Server LTS (Linux)**: Recommended for its reliability, community support, containerization, and open-source advantages.

### 2. **System Architecture**  
Use a **monolithic kernel** for performance with modular extensions. Employ a **client-server model** with RESTful/WebSocket APIs for real-time interaction.

### 3. **Storage Management**  
Adopt **XFS with LVM** and integrate cloud storage (AWS S3, Google Cloud). Use encryption at rest and ensure auto-scaling.

### 4. **Memory Management**  
Linux virtual memory with OOM, swap, and slab allocation. Assign memory quotas per container to manage spikes in demand.

### 5. **Distributed Systems**  
Use **microservices**, containerized with Docker and orchestrated with Kubernetes. Include load balancers, service discovery, and heartbeat monitoring.

### 6. **Security**  
Implement AES-256 for data at rest, TLS/SSL for transit. Use bcrypt or Argon2 for hashing, OAuth 2.0/JWT for auth, and tools like OSSEC and firewalls for endpoint protection.

## 🗂️ Document Revision History

| Version | Date       | Author     | Comments                      |
|---------|------------|------------|-------------------------------|
| 1.0     | 06/24/2025 | Adil Patel | Initial submission            |

