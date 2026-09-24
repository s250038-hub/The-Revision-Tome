# 📖 The Revision Tome — AI Study Revision Generator
## Online website : https://s250038-hub.github.io/The-Revision-Tome/
**Smart Revision Tome** is an interactive, browser-based revision set generator that transforms study materials—including lecture slides, text documents, and photo notes—into custom practice examinations with multiple choice questions and long/essay answer rubrics.

Built with an antique parchment aesthetic and powered by the **Google Gemini 3 Flash API**, it seamlessly handles multi-file parsing, auto-detects content languages (including Traditional Chinese and English), and provides offline fallback capabilities.

## ✨ Features

* **📄 Multi-Format File Parsing (Client-Side)**

  * **PDF Documents:** Page-by-page text extraction powered by `PDF.js`.

  * **PPTX Presentations:** Slide XML decomposition using `JSZip`.

  * **Image Notes & Photos:** Optical Character Recognition (OCR) via `Tesseract.js` for handwritten/scanned notes.

  * **Multi-file Upload:** Supports loading and merging multiple files in a single session.

* **🤖 AI-Powered Question Synthesis**

  * **Gemini 3 Flash Integration:** Uses structured JSON schema output to produce high-quality MCQs and essay questions.

  * **Strict Language Auto-Detection:** Automatically detects document language (e.g., Traditional Chinese `zh-TW` vs. English `en`) and enforces uniform language generation across all questions, options, and rationales.

  * **Offline/Resilient Fallback:** Includes a local NLP synthesizer if network or API limits are encountered.

* **📝 Interactive Revision Experience**

  * **Multiple Choice Questions (MCQs):** Real-time scoring, instant answer feedback, and detailed rationale explanations.

  * **Long / Essay Questions:** Complete with model response outlines and self-assessment rubric checklists.

  * **Scratchpad:** On-screen response note pad for drafting essay answers before revealing solutions.

* **🎨 Vintage Tome Aesthetic & Print Support**

  * Custom parchment textures, typography (`Cinzel` & `Lora`), and wax seal visual indicators.

  * CSS `@media print` styling optimized for printing clean revision worksheets without UI clutter.

## 🛠️ Tech Stack & Libraries

| Category | Technology / Library | Description | 
 | ----- | ----- | ----- | 
| **Styling** | [Tailwind CSS](https://tailwindcss.com/?utm_source=gemini "null") | Responsive UI with custom vintage parchment styling | 
| **Typography** | [Google Fonts](https://fonts.google.com/?utm_source=gemini "null") | `Cinzel`, `Lora`, and `Inter` | 
| **Icons** | [Lucide Icons](https://lucide.dev/?utm_source=gemini "null") | Feather-based lightweight UI iconography | 
| **PDF Processing** | [PDF.js](https://mozilla.github.io/pdf.js/?utm_source=gemini "null") | In-browser PDF text parsing worker | 
| **PPTX Parsing** | [JSZip](https://stuk.github.io/jszip/?utm_source=gemini "null") | Unpacks `.pptx` XML slides directly in browser | 
| **Image OCR** | [Tesseract.js](https://tesseract.projectnaptha.com/?utm_source=gemini "null") | In-browser OCR for images (`.png`, `.jpg`, `.jpeg`) | 
| **AI Model** | [Google Gemini 3 Flash](https://ai.google.dev/?utm_source=gemini "null") | High-speed structured response generation | 

## 🚀 Quick Start & Usage

Because the application is built as a single-file web application, **no installation or server setup is required**.

### 1. Running the Application

Simply double-click `index.html` or open it in any modern web browser (Chrome, Edge, Firefox, Safari).

### 2. Generating a Revision Exam

1. **Upload Notes:** Drag and drop your files (PDFs, PPTX slides, or image notes) onto the left page dropzone.

2. **Set Targets:** Choose the desired quantity of Multiple Choice Questions and Long/Essay Questions.

3. **Generate:** Click **"Generate Revision Set"**.

4. **Practice & Review:**

   * Click option buttons on the right page to test your knowledge in real time.

   * Switch tabs to practice essay prompts and verify against the marking rubrics.

   * Use the **Print** button to export a paper worksheet version.

## 📋 File Structure

```
.
├── index.html       # Primary application file (Includes HTML, CSS, JavaScript & Gemini API integration)
└── README.md        # Documentation

```

## 🔒 Privacy & Local Processing

* All file parsing (PDF text extraction, PPTX unzipping, OCR) is performed **entirely client-side inside your browser**.

* Only the extracted text content is sent to the Gemini API endpoint for question generation.

## 📜 License

Distributed under the MIT License. Feel free to modify and extend for personal academic or educational use!
