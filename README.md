# Intelligent Screenshot-to-Text Chrome Extension

## Overview

This project is a Chrome extension that allows users to select any region of their screen — such as text in YouTube videos, posters, presentations, PDFs, or images — and instantly convert it into editable, copyable text using Optical Character Recognition (OCR).

Unlike traditional screenshot tools, this extension goes beyond basic text extraction. It intelligently analyzes the detected content and adapts its processing based on the detected modality. For example, if the selected region contains plain text, it returns clean, formatted paragraphs. If it detects source code, it reconstructs indentation, corrects minor OCR errors, and formats the output according to the detected programming language to preserve readability and structure.

The goal is to transform static visual text into structured, usable digital content — effectively bridging the gap between pixels and editable information.

---

## Key Features

- 📸 Region-based screenshot selection  
- 🔎 OCR-powered text extraction  
- 🧠 Content-aware post-processing  
- 📋 One-click copy to clipboard  
- ⚡ Fast, browser-native experience  

---

## Intelligent Content Modes

### 1. Plain Text Mode
- Extracts and cleans paragraph text  
- Normalizes whitespace and line breaks  
- Applies basic spell correction (optional)  

### 2. Code Mode
- Detects programming syntax patterns  
- Reconstructs indentation using spatial layout  
- Fixes common OCR character errors (`l` vs `1`, `O` vs `0`, etc.)  
- Formats output using language-specific formatters  

### 3. Math Mode
- Detects mathematical symbols and expressions  
- Converts output into LaTeX or structured mathematical text  

### 4. Table Mode
- Identifies column alignment patterns  
- Reconstructs structured tables  
- Exports as CSV or Markdown table  

### 5. Handwriting Mode (Optional)
- Uses handwriting-aware OCR  
- Converts notes into clean digital text  

---

## Technical Architecture (High-Level)

### 1. Screenshot Capture
- Chrome Extension APIs (`chrome.tabs.captureVisibleTab`)
- Custom region selection overlay
- Canvas-based cropping

### 2. OCR Engine
- Client-side OCR (e.g., Tesseract.js)  
  *or*  
- Backend-based OCR (EasyOCR / PaddleOCR / Vision APIs)

### 3. Post-Processing Pipeline
- Layout-aware reconstruction using bounding box coordinates  
- Content-type detection (heuristics or lightweight classifier)  
- Mode-specific formatting and correction  

---

## Future Enhancements

- Real-time subtitle extraction from videos  
- Automatic language detection  
- Direct export to GitHub Gist  
- LLM-based correction for improved code accuracy  
- Confidence scoring with visual heatmaps  

---

## Vision

The web is full of valuable information trapped inside images and videos. This extension aims to unlock that data, making it editable, searchable, and reusable — turning pixels into structured knowledge.
