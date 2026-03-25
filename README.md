# 🔍 PlagiScan AI — Intelligent Plagiarism Detection System

> A Final Year Project by **[Yash Khatri](https://theyashkhatri.dev)**

---

## 📌 Project Description

**PlagiScan AI** is an AI-powered plagiarism detection web application built as a Final Year Computer Science project. It leverages **Google Gemini 1.5 Flash** (a state-of-the-art large language model) to analyze submitted text and produce detailed plagiarism reports — including similarity scores, matched sources, highlighted suspicious phrases, paraphrase detection, and AI-written content detection.

Unlike traditional plagiarism checkers that rely purely on string matching against a fixed database, PlagiScan AI uses deep semantic understanding to detect:
- **Verbatim copying** from web articles, Wikipedia, academic papers, and textbooks
- **Paraphrased content** where ideas are borrowed but reworded
- **AI-generated writing** patterns typical of large language models
- **Near-duplicate sentences** with minor word substitutions

The entire application runs as a **single HTML file** — no server, no installation, no backend required.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔬 AI-Powered Analysis | Uses Google Gemini 1.5 Flash for deep semantic plagiarism detection |
| 📊 Similarity Score | Animated ring meter showing 0–100% similarity with color-coded verdict |
| 🎨 Highlighted Text | Flagged phrases highlighted in red (high), yellow (moderate), blue (paraphrased) |
| 📰 Matched Sources | List of detected source URLs with individual match percentages |
| 💡 Smart Suggestions | Actionable recommendations based on what was found |
| 📋 Full Formal Report | 200+ word professional academic plagiarism report |
| 📎 File Upload | Drag & drop or click to upload `.txt` files |
| ⚙️ Analysis Options | Toggle Web Sources, Academic DB, Paraphrase & AI-Written detection |
| 🎯 Sensitivity Modes | Standard, Strict, and Lenient analysis modes |
| ⬇️ Export Report | Download complete report as `.txt` file |
| 🔒 Secure Key Storage | API key stored in browser `localStorage` — never leaves your device |
| 📱 Responsive Design | Works on desktop, tablet, and mobile |

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- A free Google Gemini API key

### Step 1 — Get a Free API Key
1. Go to 👉 **[aistudio.google.com/apikey](https://aistudio.google.com/apikey)**
2. Sign in with your Google account
3. Click **"Create API Key"**
4. Copy the key (starts with `AIzaSy...`)

> ✅ Completely free — no credit card required. 15 requests/minute on the free tier.

### Step 2 — Run the App
1. Download `plagiarism-checker.html`
2. Open it in any web browser (double-click or drag into browser)
3. Paste your API key in the **🔑 API Configuration** field
4. Paste or upload your text
5. Click **"Analyze for Plagiarism"**

> No npm install. No server. No dependencies. Just open and use.

---

## 🧪 Test Cases

Use these samples to test the application:

### Test 1 — High Plagiarism (~70%)
```
Machine learning (ML) is a field of study in artificial intelligence concerned with the development and study of statistical algorithms that can learn from data and generalize to unseen data, and thus perform tasks without explicit instructions. Recently, generative artificial intelligence has become a powerful force in the field. The name machine learning was coined in 1959 by Arthur Samuel, an IBM employee and pioneer in the field of computer gaming and artificial intelligence.
```

### Test 2 — Moderate Plagiarism (~35%)
```
Machine learning is a part of artificial intelligence that focuses on building systems which can learn from data. Instead of being explicitly programmed, these systems improve their performance over time through experience. The term was first introduced by Arthur Samuel in the late 1950s when he was working at IBM on computer game programs.
```

### Test 3 — Mostly Original (~5%)
```
In my opinion, the rise of data-driven technologies has changed the way we approach problem-solving in engineering. Rather than relying solely on deterministic models, engineers today often incorporate statistical and probabilistic methods to handle uncertainty. This shift has been gradual but significant, particularly in domains like structural health monitoring and predictive maintenance.
```

### Test 4 — AI-Generated Detection (~40%)
```
Artificial intelligence is revolutionizing various industries by enabling machines to perform tasks that traditionally required human intelligence. From healthcare to finance, AI applications are transforming the way organizations operate and make decisions. The potential of AI to drive innovation and improve efficiency is immense, and its impact will only continue to grow in the coming years.
```

---

## 🏗️ Project Structure

```
plagiarism-checker.html     ← Entire application (single file)
README.md                   ← This file
```

### Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| AI Engine | Google Gemini 1.5 Flash API |
| Fonts | Syne (display), DM Mono (code), DM Sans (body) |
| Storage | Browser localStorage (API key only) |
| Hosting | Any static host or local file system |

---

## ⚙️ How It Works

```
User Input (text / file)
        ↓
Tokenization & Word Count
        ↓
Prompt Engineering (system + user prompt)
        ↓
Google Gemini 1.5 Flash API
        ↓
JSON Response Parsing
        ↓
Similarity Score Calculation
  (flagged words / total words × 100)
        ↓
Results Rendering
  ├── Highlighted Text View
  ├── Matched Sources List
  ├── Suggestions Panel
  └── Full Formal Report
```

### Scoring Thresholds

| Score | Verdict | Meaning |
|---|---|---|
| 0 – 10% | ✅ Mostly Original | Only common phrases, no meaningful plagiarism |
| 11 – 25% | 🟡 Minor Plagiarism | A few lifted phrases, mostly original work |
| 26 – 50% | 🟠 Moderate Plagiarism | Notable copied/paraphrased sections |
| 51 – 100% | 🔴 Highly Plagiarized | Majority of text is copied or AI-generated verbatim |

---

## 🔐 Privacy & Security

- Your API key is stored **only in your browser's `localStorage`**
- Text submitted for analysis is sent **directly to Google's API** — it does not pass through any third-party server
- No user data is collected, stored, or logged anywhere
- The app has **no backend** — it is 100% client-side

---

## 📸 UI Overview

- **Dark forensic theme** with amber accent colors
- **Animated progress bar** with live step-by-step status
- **SVG ring meter** for similarity score visualization
- **4-tab results panel** — Highlighted Text, Sources, Suggestions, Full Report
- **Responsive grid layout** for all screen sizes

---

## 🙋 Author

**Yash Khatri**
🌐 [theyashkhatri.dev](https://theyashkhatri.dev)

---

## 📄 License

This project is developed as an academic Final Year Project. Free to use for educational and demonstration purposes.

---

> 💡 **Tip for demo day:** Clear `localStorage` before presenting so the API key prompt appears fresh. Run the 4 test cases above in order to showcase all verdict levels cleanly.
