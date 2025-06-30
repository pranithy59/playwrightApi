
# 📘 Bookstore API Automation with Playwright + TypeScript

This repository contains an end-to-end API test automation framework built with **Playwright** and **TypeScript**, targeting a **FastAPI-based Bookstore API**.

## 📦 Project Structure

```
bookstore-api-playwright/
├── .env                     # Environment variables
├── .gitignore
├── package.json             # Project metadata and dependencies
├── package-lock.json
├── playwright.config.ts     # Playwright configuration file
├── tsconfig.json            # TypeScript configuration file
├── README.md
├── tests/                   # Test files organized by features or endpoints
├── utils/                   # Utility functions for request payloads, data, etc.
└── .github/
    └── workflows/ci.yml     # GitHub Actions CI configuration
```

## 🚀 Getting Started

### 📁 Prerequisites

Ensure you have the following installed:

- Node.js (v16+)
- npm
- Python 3.8+ (to run the FastAPI server)
- FastAPI & Uvicorn

### ▶️ Starting the FastAPI Server

```bash
uvicorn main:app --reload
```

Ensure the server is running on `http://127.0.0.1:8000` as the tests are configured for this endpoint.

### ▶️ Install Dependencies

```bash
npm install
```

### ▶️ Run Tests

```bash
npx playwright test
```

### ▶️ View Test Report

```bash
npx playwright show-report
```

## ✅ Features & Test Coverage

The framework currently supports:

- **Create Book** (with valid and invalid data)
- **Get Book by ID** and **list all books**
- **Update Book** (including error handling for invalid payloads)
- **Delete Book** (handling valid and invalid IDs)
- **Request chaining** to test sequence-dependent actions
- **Assertions** on headers, payloads, and HTTP status codes

## 🧪 Tech Stack

- [Playwright](https://playwright.dev/) for API testing
- [TypeScript](https://www.typescriptlang.org/) for type-safe code
- [FastAPI](https://fastapi.tiangolo.com/) backend (test target)
- [GitHub Actions](https://docs.github.com/en/actions) for CI/CD

## 🔁 Continuous Integration

CI is powered by **GitHub Actions**. On each push to the `main` branch:

1. Dependencies are installed
2. Tests are executed
3. Reports are uploaded

Configuration can be found in `.github/workflows/ci.yml`.

