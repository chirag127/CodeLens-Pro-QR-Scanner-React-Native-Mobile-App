# CodeLens-Pro-QR-Scanner-React-Native-Mobile-App

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App/ci.yml?style=flat-square)](https://github.com/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App/actions/workflows/ci.yml)
[![Coverage](https://img.shields.io/codecov/c/github/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App?style=flat-square)](https://codecov.io/gh/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App)
[![License](https://img.shields.io/github/license/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App?style=flat-square)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App?style=flat-square)](https://github.com/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App)
[![Language](https://img.shields.io/github/languages/top/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App?style=flat-square)](https://github.com/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App)
[![Topics](https://img.shields.io/github/topics/react-native,typescript,qr-code-scanner?style=flat-square)](https://github.com/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App)

> **Star ⭐ this Repo** if you appreciate high-performance, native-optimized mobile scanning solutions.

---

A professional, high-performance QR code scanner mobile application built leveraging the **Apex Toolchain** for React Native, ensuring cross-platform consistency on iOS and Android. It features low-latency, real-time scanning via native modules, intelligent content parsing, and secure, performance-driven history persistence using MMKV.

This repository adheres to the **Elite Architect Standard (December 2025)**, emphasizing strict TypeScript usage, declarative UI construction, and hardware-accelerated performance.

## 🏗️ Architecture Overview

The application follows the **Feature-Sliced Design (FSD)** pattern for modularity and scalability, crucial for large-scale mobile development. The use of `react-native-vision-camera` guarantees maximum frame-rate capture, minimizing latency.

mermaid
graph TD
    A[User Input / Device Camera] -->|Raw Frames (Native)| B(VisionCamera Module)
    B -->|Process Frame| C{Scan & Decode Logic}
    C -- Success --> D[Content Detection & Contextual Action Engine]
    C -- Failure --> A
    D -- Valid Data --> E(State Management: Zustand/Reanimated)
    D -- History Required --> F[(MMKV Persistence Layer - Secure History)]
    E --> G[UI Layer: NativeWind/React Native Elements]
    G --> H[Output: Display Results / Execute Action]
    F --> E


## 📋 Table of Contents

1.  [CodeLens-Pro-QR-Scanner-React-Native-Mobile-App](#codelens-pro-qr-scanner-react-native-mobile-app)
2.  [🏗️ Architecture Overview](#-architecture-overview)
3.  [📋 Table of Contents](#-table-of-contents)
4.  [🚀 Key Features](#-key-features)
5.  [🛠️ Technology Stack (Apex Toolchain 2026)](#-technology-stack-apex-toolchain-2026)
6.  [✨ Development & Setup](#-development--setup)
7.  [🤖 AI Agent Directives (Internal Specification)](#-ai-agent-directives-internal-specification)
8.  [📜 License](#-license)

## 🚀 Key Features

*   **Ultra-Low Latency Scanning:** Utilizes `react-native-vision-camera` integrated directly with native libraries for superior frame processing speed.
*   **Intelligent Content Parsing:** Differentiates between URLs, Contact Cards (vCard), Wi-Fi credentials, and raw text automatically.
*   **Contextual Actions:** Presents immediate, actionable buttons based on decoded content (e.g., 'Open Link', 'Add Contact', 'Connect to Wi-Fi').
*   **Performance Storage:** Securely and rapidly stores scan history using **MMKV** for native-speed local persistence, avoiding SQLite overhead for simple key-value lookups.
*   **Modern Styling:** Built using **NativeWind** for utility-first, highly performant styling that compiles efficiently to native components.
*   **Cross-Platform Fidelity:** Engineered for seamless operation and visual parity on both iOS and Android.

## 🛠️ Technology Stack (Apex Toolchain 2026)

| Category | Technology | Version/Standard |
| :--- | :--- | :--- |
| **Core Framework** | React Native | Latest Stable (Native Driver Focus) |
| **Language** | TypeScript | Strict Mode (5.x/6.x) |
| **Toolchain Manager**| Expo (Managed/Bare) | Optimized for Native Module Integration |
| **Camera Core** | react-native-vision-camera | Native Performance Focus |
| **Styling** | NativeWind (TailwindCSS) | Utility-First, JIT Compilation |
| **State/Animations** | Zustand, React Native Reanimated | Fluid UI Transitions |
| **Persistence** | MMKV | High-Speed Local Storage |
| **Linting/Formatting**| Biome | Speed and Unified Configuration |

## ✨ Development & Setup

This project requires Node.js (20+), Watchman, and the relevant native environments (Xcode/Android Studio).

1.  **Clone Repository:**
    bash
    git clone https://github.com/chirag127/CodeLens-Pro-QR-Scanner-React-Native-Mobile-App.git
    cd CodeLens-Pro-QR-Scanner-React-Native-Mobile-App
    

2.  **Environment Setup (using `uv` principles for dependency management simulation in RN context):**
    bash
    # Install dependencies
    npm install 
    # Or yarn/pnpm install
    

3.  **Verification & Build Scripts:**

| Command | Description | 
| :--- | :--- |
| `npm run clean` | Clears Metro cache and native build artifacts. |
| `npm run lint` | Runs Biome checks across the codebase. |
| `npm run test:unit` | Executes Vitest unit tests for logic modules. |
| `npm run test:e2e` | Runs Playwright or Maestro end-to-end simulation. |
| `npm run start` | Starts the Metro bundler for development. |
| `npm run ios` | Builds and runs the application on an iOS simulator/device. |
| `npm run android` | Builds and runs the application on an Android emulator/device. |

### Development Principles

*   **SOLID:** Applied rigorously, especially in the Content Detection Engine.
*   **DRY:** Maximized via shared utility functions and NativeWind configuration.
*   **YAGNI:** Features are only implemented when demanded by clear user feedback or performance analysis.

## 🤖 AI Agent Directives (Internal Specification)

<details>
<summary>Apex Agent Configuration & Verification (December 2025)</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs. Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** This repository is a **Mobile Application** built with React Native/TypeScript.

*   **PRIMARY SCENARIO: WEB / APP / GUI (Modern Frontend - Mobile Variant)**
    *   **Stack:** TypeScript 6.x (Strict/Recommended Config), React Native (Latest), **Vite/Metro (Bundler)**, **NativeWind** (Styling), **Biome** (Linter/Formatter).
    *   **Lint/Test:** **Biome** (Speed/Config Validation) + **Vitest** (Unit Tests for logic layers) + **Playwright/Maestro** (E2E).
    *   **Architecture:** **Feature-Sliced Design (FSD)** is mandatory for organizing features, layers (e.g., `entities`, `features`, `pages`).

---

## 4. VERIFICATION & EXECUTION PROTOCOL
*   **BUILD VERIFICATION:** Always prioritize the outcome of `npm run build:prod` or equivalent production artifact generation.
*   **PERFORMANCE TARGET:** Scanning latency must remain under 100ms for a standard QR code decode on mid-range devices (Q3 2024 baseline).
*   **TYPE SAFETY:** Any code modification must maintain 100% type safety across all transitions between Native and JS bridge layers.

</details>

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License**. See the [LICENSE](./LICENSE) file for details.

`Copyright © 2024 chirag127. This project is licensed under CC BY-NC 4.0.`