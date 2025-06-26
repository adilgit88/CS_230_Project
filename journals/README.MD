
# Draw It or Lose It – Final Software Design Portfolio

## 📘 Overview

This repository contains all journal reflections and the final Software Design Document for the course **CS 230: Software Design and Engineering** at Southern New Hampshire University. The project focuses on redesigning *Draw It or Lose It*—originally an Android-exclusive game—for web, desktop, and mobile platforms using scalable, secure, and distributed architecture principles.

## 🗂 Contents

- ✅ Module 4 Journal – Client-Server Architecture Reflection
- ✅ Final Software Design Document (Module 8)
- ✅ Design Patterns: Singleton and Iterator
- ✅ Domain Model and Evaluation Matrix
- ✅ Platform Recommendation and System Architecture Proposal

## 🎯 Project Objective

Redesign **Draw It or Lose It** to:
- Be platform-independent (web, desktop, mobile)
- Support multiple teams and players
- Enforce unique identifiers across entities
- Use a centralized game instance (Singleton pattern)
- Operate in a secure, distributed environment

## 📄 Software Design Document Summary

### Executive Summary
The Gaming Room seeks to expand its *Draw It or Lose It* game across platforms. This document outlines a modular Java-based software design using design patterns and a Linux server infrastructure to support real-time, scalable, and secure gameplay.

### Requirements
- Unique names for game, team, and player
- Multiple teams and players per game
- Single game instance at a time (Singleton)
- Prevent duplication of entity names

### Design Constraints
- Real-time distributed communication
- Cross-platform compatibility
- Synchronization across all clients
- Security and performance optimization

### Domain Model
- **Entity superclass**: `id`, `name`
- **Game** → List of Teams  
- **Team** → List of Players  
- **Design Patterns**: Singleton (game instance), Iterator (navigation)

### Evaluation
Includes comparison of platform suitability for:
- Server & Client roles
- Development tools
- Compatibility
- Scalability & resource handling

### Recommendations
- **Platform**: Linux (Ubuntu Server LTS)
- **Architecture**: Client-server with microservices (Docker + Kubernetes)
- **Storage**: Cloud-based (Amazon S3, Azure Blob), with local LVM/XFS
- **Memory**: Paging, OOM protection, container memory limits
- **Networking**: REST APIs + WebSockets for real-time features
- **Security**: TLS, AES-256 encryption, OAuth2/JWT, bcrypt, OSSEC

## 🧠 Reflection Highlights

- Reinforced understanding of client-server architecture and RESTful API design
- Learned how design patterns like Singleton and Iterator can be used for control and traversal
- Explored distributed architecture strategies using containers and orchestration tools
- Gained insight into securing data through encryption, hashed credentials, and authentication protocols

## 📅 Document Revision History

| Version | Date       | Author      | Comments                                    |
|---------|------------|-------------|---------------------------------------------|
| 1.0     | 05/22/2025 | Adil Patel  | Initial submission with full design document |
| 2.0     | 06/12/2025 | Adil Patel  | Updated Evaluation and Recommendations       |

## 📚 Course Information

- **Course**: CS 230 – Software Design and Engineering  
- **Institution**: Southern New Hampshire University  
- **Term**: Summer 2025  
- **Student**: Adil Patel  

