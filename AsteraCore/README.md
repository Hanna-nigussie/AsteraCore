# AsteraCore: Enterprise Event-Sourced Financial Infrastructure

[![CI](https://github.com/AsteraCore/AsteraCore/actions/workflows/ci.yml/badge.svg)](https://github.com/AsteraCore/AsteraCore/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/downloads/)
[![Docker](https://img.shields.io/badge/docker-✓-blue.svg)](https://www.docker.com/)
[![Kubernetes](https://img.shields.io/badge/kubernetes-✓-blue.svg)](https://kubernetes.io/)
[![Event Sourcing](https://img.shields.io/badge/event--sourcing-✓-green.svg)](https://martinfowler.com/eaaDev/EventSourcing.html)

## 🚀 Overview

**AsteraCore** is a comprehensive, production-ready financial infrastructure platform designed for secure digital identity, financial services, and operational trust. It brings together the core capabilities needed for modern enterprise-grade infrastructure in a unified, event-sourced system:

| Challenge Area                           | Implementation                                                                               |
| ---------------------------------------- | -------------------------------------------------------------------------------------------- |
| **A. AI-Driven Biometric Verification**  | Face recognition, liveness detection, deepfake detection, voice biometrics, fairness metrics |
| **B. Intelligent eKYC Orchestration**    | Fayda National ID integration, OCR+NLP, synthetic identity detection, KYC portability        |
| **C. Digital Identity System**           | Identity lifecycle, selective disclosure, secure vault, identity recovery                    |
| **D. Federated SSO**                     | OAuth2/OIDC, consent management, cross-border federation, biometric-backed SSO               |
| **E. Card-Based Identity & Transaction** | Virtual cards, biometric binding, offline payments, dynamic CVV, tokenization                |

## 🏆 Key features

- **Immutable Event Store**: Every action is recorded as an append-only event — complete audit trail
- **Cryptographic Hash Chain**: SHA-256 tamper-evident security — bank-grade integrity
- **Temporal Queries**: "Time-travel" audit capability — ask "what was the state at 2:00 PM?"
- **Gas Town Pattern**: Agent memory survives crashes — zero data loss
- **Optimistic Concurrency**: Prevents double-spending — handles race conditions
- **Fayda Integration**: Native Ethiopian National ID support — local relevance
- **Offline Payments**: Sequence-protected QR vouchers — financial inclusion

---

## 🛠️ Technology Stack

| Layer              | Technology                                            |
| ------------------ | ----------------------------------------------------- |
| **Backend**        | Python 3.11, FastAPI, SQLAlchemy, Pydantic            |
| **Event Store**    | PostgreSQL 15 (append-only, immutable)                |
| **AI/ML**          | TensorFlow 2.15, OpenCV, MediaPipe, XGBoost, FaceNet  |
| **Frontend**       | Next.js 14, React, TypeScript, TailwindCSS, Shadcn UI |
| **Infrastructure** | Docker, Kubernetes, Redis, Nginx                      |
| **Security**       | OAuth2/OIDC, JWT, AES-256, Cryptography               |

---

## 🚀 Quick Start

### Prerequisites

- Docker Desktop (for local development)
- Python 3.11+
- Node.js 18+
- PostgreSQL 15 (or use Docker)

### Local Development (with Docker)

```bash
# Clone the repository
git clone https://github.com/your-org/asteracore.git
cd asteracore

# Copy environment variables
cp .env.example .env

# Start all services
docker-compose up -d

# Run migrations
make migrate

# Run tests
make test

# Access services
# Frontend: http://localhost:3000
# API Gateway: http://localhost:8000
# Event Store: postgres://localhost:5432/ethio_core
```

# 🧪 Testing

```bash
# Run all tests

# Run unit tests only
pytest modules/*/tests/ -m "not integration"

# Run integration tests
pytest modules/*/tests/ -m integration

# Run concurrency tests (critical for double-spend prevention)
pytest tests/test_concurrency.py

# Run integrity tests (hash chain verification)
pytest tests/test_integrity.py
```

