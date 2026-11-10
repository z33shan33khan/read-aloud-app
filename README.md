# 📖 Pro Reader

**Pro Reader** is a powerful, privacy-first, single-file web application that turns your browser into an advanced Text-to-Speech (TTS) document reader. It supports PDFs, EPUBs, web pages, and plain text, featuring word-level highlighting, auto-translation, offline voice caching (Piper TTS), and a persistent local library.

No build steps, no backend, and no accounts required. Everything runs locally in your browser.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-Active-success.svg)

---

## ✨ Key Features

### 📚 Advanced Document Support
- **PDF Reading:** Extracts text natively. Automatically falls back to **on-device OCR** (via Tesseract.js) for scanned or poorly encoded PDFs.
- **EPUB Support:** Parses chapters and metadata directly in the browser using JSZip.
- **Web Pages:** Fetches and cleans up web articles via Jina AI Reader for distraction-free listening.
- **Plain Text:** Supports `.txt`, `.md`, `.html`, `.rtf`, `.srt`, and `.vtt`.

### 🗣️ Professional Text-to-Speech
- **Granular Highlighting:** Choose between Word-by-Word, Sentence, Paragraph, or combined "Pro" modes that highlight the current sentence *and* the active word.
- **Custom Pronunciations:** Build a personal dictionary to fix the pronunciation of names, acronyms, or technical terms.
- **Fine-Grained Controls:** Adjustable speed (0.5x to 3.0x+), pitch, and volume, with quick-access speed presets.
- **Piper TTS Integration:** Built-in Voice Manager to download and cache high-quality, offline neural voices (like Urdu, Arabic, English) directly into your browser's IndexedDB.

### 🌍 Multilingual & Accessibility
- **Auto-Translation:** On-the-fly page translation (supports English, Spanish, French, Chinese, Japanese, Arabic, Hindi, Urdu, etc.).
- **Rich Font Support:** Pre-loaded with optimized fonts for specific scripts, including *Noto Nastaliq* (Urdu), *Amiri* (Arabic), *Noto Serif SC* (Chinese), and *Noto Sans JP* (Japanese).
- **Dark/Light Mode:** Easy on the eyes with a polished, responsive UI that respects mobile safe-area insets.

### 💾 Local Library & Persistence
- **Auto-Save:** Remembers your reading position (page and sentence) for every document.
- **Bookmarks:** Save and jump to specific locations instantly.
- **Table of Contents:** Auto-detects chapter headings and provides a navigable sidebar.
- **100% Private:** All books, settings, and cached voices are stored locally in your browser (IndexedDB / LocalStorage). Your data never leaves your device.

---

## 🚀 Quick Start

### Option 1: Direct Use (Simplest)
1. Download or clone the `index.html` file.
2. Double-click the file to open it in your web browser (Chrome, Edge, or Safari recommended).
3. Click **Open File**, paste text, or load a web URL to begin.

### Option 2: Local Server (Recommended for Web Fetching & CORS)
Some browser security policies restrict file loading or web fetching from `file://` URLs. To unlock all features:
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (npx)
npx serve .
