# Tian Chatbot

An AI-powered chatbot tool designed to help students preparing for Japanese graduate school entrance exams write research plans (研究計画書) more efficiently. The system provides real-time conversational guidance to organize ideas and refine research proposals.

## Overview

Tian Chatbot is a full-stack application consisting of a Vue 3 frontend and a Spring Boot backend. It uses Server-Sent Events (SSE) for streaming AI responses and integrates with Alibaba Cloud's DashScope (Qwen) for natural language processing.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Vue 3, Vite, Axios, Marked, DOMPurify |
| Backend | Spring Boot 4, Java 21, LangChain4j |
| AI | DashScope (Qwen) via LangChain4j |
| Build | Maven (backend), npm (frontend) |

## Project Structure

```
tian-chatbot/
├── tian-chatbot-backend/     # Spring Boot API server
│   ├── src/main/java/        # Java source code
│   └── src/main/resources/   # Configuration files
├── tian-chatbot-frontend/    # Vue 3 SPA
│   ├── src/
│   │   ├── components/      # Vue components
│   │   ├── utils/           # Utilities
│   │   └── config.js        # API configuration
│   └── public/
└── README.md
```

## Quick Start

### Prerequisites

- **Backend:** JDK 21, Maven 3.6+
- **Frontend:** Node.js 18+, npm

### 1. Start the Backend

```bash
cd tian-chatbot-backend
mvn spring-boot:run
```

The API server runs at `http://localhost:8080`.

> **Note:** Configure your DashScope API key in `application-local.yml` before running. See [Backend README](tian-chatbot-backend/README.md) for details.

### 2. Start the Frontend

```bash
cd tian-chatbot-frontend
npm install
npm run dev
```

The app is available at `http://localhost:5173`.

### 3. Use the Application

Open `http://localhost:5173` in your browser. The chat interface connects to the backend via Vite's proxy (`/api` → `localhost:8080`).

## Development

- **Backend:** See [tian-chatbot-backend/README.md](tian-chatbot-backend/README.md)
- **Frontend:** See [tian-chatbot-frontend/README.md](tian-chatbot-frontend/README.md)

## License

Private / Practice project.
