---
name: 🐛 Bug Report
about: Report an issue or unexpected behavior in the ApexScanner Mobile Application
title: "[BUG] Short, descriptive title (e.g., Scanner freezes when detecting blurred codes)"
labels: ["bug", "triage/needs-investigation"]
assignees: ""

## 1. Overview

**Describe the bug clearly and concisely.** What unexpected behavior did you observe? Does it crash, produce incorrect output, or fail to meet requirements?

---

## 2. Reproduction Steps (The Path to Failure)

Provide a step-by-step guide that allows developers to reliably reproduce the issue. The goal is 100% reproducibility.

1. **Setup:** (e.g., Device: iPhone 15 Pro, OS: iOS 18.1, App Version: v1.2.5)
2. **Action:** Launch scanner module.
3. **Trigger:** Point the camera at a QR code with the following specific content: `TEST_DATA_WITH_NEWLINE\nAND_SPECIAL_CHARACTERS!`
4. **Expected Result:** The scanner parses the content and history logs the exact string.
5. **Actual Result:** The application displays an error toast: "Parsing Error: Unexpected token at index 42", and the history remains empty.

---

## 3. Environmental Context (The Apex Platform)

Details about where the bug occurred. Specificity here accelerates diagnosis.

*   **Platform:** [ ] iOS | [ ] Android
*   **Device Model:** (e.g., Pixel 8, Samsung Galaxy S24 Ultra, iPhone 14)
*   **OS Version:** (e.g., Android 14, iOS 18.2)
*   **App Build/Version:** (Check 'About' screen in settings)
*   **Scanner Module Used:** [ ] Real-Time (Continuous) | [ ] Single Capture
*   **QR Code Type:** [ ] Standard Alphanumeric | [ ] Wi-Fi Config | [ ] Contact Card | [ ] Other (Specify: ______)

---

## 4. Supporting Evidence

Attach relevant logs, screenshots, or screen recordings.

*   **Screenshots/Videos:** (Drag and drop files here or link to an external host)
*   **Relevant Log Snippets (from device logs or crash reporter):**


// Paste any relevant error stack traces or console output here. 
// If using a native module, please include logs from XCode/Android Studio.
//


---

## 5. Architectural Impact Assessment (Self-Analysis)

*(Optional, but highly appreciated by the Apex Architects)*

Based on your understanding, which part of the stack do you suspect is impacted?

*   [ ] **Native Module Bridge** (Communication between JS and Native)
*   [ ] **Core Scanning Library** (e.g., `react-native-camera` integration)
*   [ ] **Content Parsing Logic** (Post-capture validation)
*   [ ] **Persistent Storage** (`MMKV` integration/read)
*   [ ] **UI/Rendering** (Display artifacts)
*   [ ] **Other (Specify):**

---

## 6. Resolution Suggestions (If Applicable)

Do you have an idea on how to fix this? Reference any relevant GitHub commits or known external library fixes if possible.


// Suggestion here

