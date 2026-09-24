# 📖 The Revision Tome — Multimodal AI Study Generator

**The Revision Tome** is an interactive, browser-based revision set generator that transforms entire study documents—including lecture slides (`.pptx`), multi-page PDF documents (`.pdf`), and photo/handwritten notes (`.png`, `.jpg`, `.webp`)--into custom practice exams complete with Multiple Choice Questions and Long/Essay Question rubrics.

Designed with an antique parchment aesthetic, it leverages the **Google Gemini 3 Flash Multimodal API** to process entire binary file payloads (diagrams, tables, formulas, and text layout) directly within a responsive two-page book interface.

## ✨ Core FeaturesQ

* **👁️ Full Multimodal Document Processing**

  * **Native Binary Payload Transmission:** Sends full Base64 document buffers (`application/pdf`, `image/*`) directly to Gemini AI so the model can visually "see" diagrams, tables, mathematical equations, and handwritten notes.

  * **PPTX Slide XML Unpacking:** Parses `.pptx` presentations directly in the browser using `JSZip`.

  * **Client-Side PDF Pre-processing:** Leverages `PDF.js` for instant language detection and text previews before API transmission.

* **🌐 Automated Language Detection & Enforcement**

  * Automatically scans document text for Chinese character density.

  * Enforces strict language output across all questions, options, detailed rationales, model answers, and rubrics—supporting both **Traditional Chinese (`zh-TW`)** and **English (`en`)**.

* **📜 Vintage Tome UI & Interactive Exam Suite**

  * **Two-Page Book Layout:** Left page dedicated to source document dropzone & target count controls; Right page serves as an unsealable practice exam.

  * **Interactive MCQs:** Instant option evaluation, real-time score tracking, and expanded rationale explanations.

  * **Essay Prompts & Rubric Checklists:** Structured long-form prompts with collapsible model answer outlines and interactive self-assessment checkboxes.

* **🖨️ Paper Worksheet Export**

  * Built-in print stylesheets (`@media print`) format the revision questions cleanly for printing or saving as a PDF worksheet without website headers or UI controls.

## 🛠️ Tech Stack & Libraries

| Category | Technology / Library | Usage | 
 | ----- | ----- | ----- | 
| **Styling** | [Tailwind CSS](https://tailwindcss.com/?utm_source=gemini "null") | Responsive UI with parchment gradients & shadows | 
| **Typography** | [Google Fonts](https://fonts.google.com/?utm_source=gemini "null") | `Cinzel`, `Lora`, and `Inter` for authentic book typography | 
| **Iconography** | [Lucide Icons](https://lucide.dev/?utm_source=gemini "null") | Clean, feather-style interface icons | 
| **PDF Parsing** | [PDF.js](https://mozilla.github.io/pdf.js/?utm_source=gemini "null") | In-browser PDF buffer extraction & page reading | 
| **PPTX Parsing** | [JSZip](https://stuk.github.io/jszip/?utm_source=gemini "null") | Unpacks `.pptx` presentation XML directly in-browser | 
| **AI Model** | [Google Gemini 3 Flash](https://ai.google.dev/?utm_source=gemini "null") | Structured JSON multimodal synthesis | 

## 🚀 Quick Start Guide

Because **The Revision Tome** is built as a self-contained web application, no compilation or backend server setup is required.

1. **Open the Application:** Launch `index.html` in any modern web browser (Chrome, Edge, Firefox, Safari).

2. **Upload Study Materials:** Drag and drop your PDFs, slide decks, or photo notes into the **Source Documents** page on the left.

3. **Configure Targets:** Set your desired number of Multiple Choice Questions and Essay/Long Questions.

4. **Unseal the Tome:** Click **"Generate Revision Set"** to trigger Gemini AI synthesis.

5. **Practice & Self-Assess:** Solve questions on the right page, review rationales, and check off rubric points for long-answer practice.

## 📂 File Structure

```
.
├── index.html       # Primary application file (Single-file HTML, CSS, JS & Gemini API integration)
└── README.md        # Documentation

```

## 🔒 Privacy & Safety

* File parsing and Base64 buffer encoding occur **100% inside your local browser instance**.

* Only the uploaded document buffers required for synthesis are submitted to the Gemini API endpoint.

## 📜 License

Distributed under the MIT License. Feel free to customize and expand for personal study or classroom instruction!