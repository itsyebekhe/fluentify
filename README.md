
[English](./README.md) | [فارسی (Persian)](./README.fa.md)
---

# Fluentify - Modern AI Translator

**Fluentify** is a powerful, all-in-one translation tool that leverages the cutting-edge capabilities of the Google Gemini AI. It provides a modern, fast, and user-friendly interface to translate text, images, PDF documents, and video subtitles with unparalleled accuracy and context-awareness.

## ✨ Core Features

Fluentify is packed with features designed for both casual users and professionals who need advanced control over their translations.

### 🌐 **Multiple Translation Modes**
- **Text Translation**: Instantly translate typed or pasted text with support for over 130 languages.
- **Image Translation (OCR)**: Automatically extract and translate text from any image (PNG, JPG, WEBP).
- **PDF Translation**: A robust PDF translation suite.
  - **Selective Translation**: Visually select specific pages or all pages to translate.
  - **Combine Pages**: Merge selected pages into a single, continuous text before translation for better context.
  - **Scanned PDF Support**: Built-in OCR to extract text from scanned documents or image-based PDFs.
  - **Batch Processing**: Translates large documents page-by-page or in chunks with a live progress bar and cancellation support.
- **Subtitle Translation**: A comprehensive toolkit for video subtitle localization.
  - **Multiple Formats**: Supports `.srt`, `.vtt`, `.ssa`, and `.ass` file formats.
  - **YouTube Integration**: Fetch subtitles directly from any YouTube video URL.
  - **Interactive Editor**: View, edit, and translate subtitles line-by-line in a clean table interface.
  - **Batch Translation**: Translate all subtitle lines at once with configurable batch sizes to manage API usage.
  - **Advanced Editing Tools**:
    - **Find & Replace**: Quickly correct names, terms, or phrases across the entire file.
    - **Automatic Line Breaking**: Split long lines to meet character-per-line standards for better readability.
  - **Export**: Download the translated subtitles in their original format, ready to be used.

### ⚙️ **Advanced Customization & Control**
- **AI Model Selection**: Choose from the latest Google Gemini models (`gemini-2.5-pro`, `gemini-2.5-flash`, etc.).
- **Translation Specialization**: Improve accuracy for specific fields like *Medical, Legal, IT, or Finance*.
- **Tone & Style Control**: Define the desired tone of the translation—*Formal, Informal, Poetic, Simple*, or provide your own **Custom Instructions**.
- **Creativity Adjustment**: Fine-tune the AI's creativity (temperature) for more literal or more creative translations.
- **Custom Prompts**: Power users can write their own translation prompts, using placeholders for dynamic content. Includes an AI-powered **Prompt Optimizer** to improve your custom instructions.

### 🚀 **User Experience & Configuration**
- **Sleek Interface**: Modern, responsive design with both **Dark and Light modes**.
- **Save Settings**: All your preferences, including your API key and chosen settings, can be saved in your browser for future use.
- **API Key Management**: Securely enter your API key with a visibility toggle.
- **Proxy Support**: Bypass regional restrictions or CORS issues by routing API requests through a proxy. Compatible with Cloudflare Workers or other proxy services.
- **Live Activity Log**: Monitor the app's operations in real-time, from API calls to OCR processing, for full transparency.
- **No Server Needed**: Runs entirely in your browser. Your files and API key are never uploaded to a third-party server.

---

## 🚀 How to Use

### 1. Initial Setup

Before you can start translating, you need a Google AI API Key.

1.  **Get an API Key**:
    - Go to [Google AI Studio](https://aistudio.google.com/).
    - Sign in with your Google account.
    - Click **"Get API key"** and then **"Create API key in new project"**.
    - Copy the generated key.
2.  **Configure Fluentify**:
    - Open Fluentify.
    - Click on **"Advanced Settings"**.
    - Paste your API key into the **"Google AI API Key"** field.
    - **(Recommended)** Check the **"Save all settings in this browser"** box at the bottom. This will securely store your key and preferences so you don't have to enter them again.

You are now ready to translate!

### 2. Translating Content

Select your desired input type from the top menu: **Text, Image, PDF, or Subtitle**.

#### **📝 Text Translation**
1.  Select the **Text** tab.
2.  Choose the source and target languages. "Auto-detect" is available for the source language.
3.  Type or paste your text into the input box.
4.  Click **Translate**.
5.  After translation, use the **Refine** and **Change Style** buttons to enhance the output.

#### **🖼️ Image Translation**
1.  Select the **Image** tab.
2.  Choose the target language. The source language will be auto-detected from the image text.
3.  Drag and drop an image file onto the app, or click **"Choose File"** to select one.
4.  Click **Translate**. The app will first perform OCR to extract text and then translate it.

#### **📄 PDF Translation**
1.  Select the **PDF** tab.
2.  Choose the target language.
3.  Upload your PDF file. The app will render a preview of all pages.
4.  Click on the pages you want to translate. They will be highlighted with a blue border. Use **"Select All"** or **"Deselect All"** for convenience.
5.  **Options**:
    - **Combine selected pages**: Check this to merge the text from all selected pages before sending it for translation. This provides better context and flow, especially for long documents.
    - **Use OCR for scanned pages** (in Advanced Settings): Enable this if your PDF contains images or scanned text.
6.  Click **Translate**. A progress bar will show the status of the operation.

#### **🎬 Subtitle Translation**
You can either upload a file or fetch subtitles from YouTube.

**Method 1: Uploading a File**
1.  Select the **Subtitle** tab.
2.  Drag and drop your `.srt`, `.vtt`, `.ssa`, or `.ass` file, or use the file picker.
3.  The **Subtitle Editor** will appear, showing all your subtitle lines.

**Method 2: Fetching from YouTube**
1.  Select the **Subtitle** tab.
2.  Paste the YouTube video URL into the input field.
3.  Enter the language code for the subtitles you want to fetch (e.g., `en` for English, `es` for Spanish).
4.  Click **Fetch**. The editor will be populated with the video's subtitles.

**Using the Subtitle Editor**
1.  **Translate**:
    - To translate everything, click the **"Translate All"** button. The app will process the lines in batches.
    - To translate a single line, click the "Translate" button on its corresponding row.
2.  **Edit**: You can manually edit any text in the "Translated Text" column by clicking on it.
3.  **Tools**:
    - **Find & Replace**: Click the magnifying glass icon, enter the text to find and the text to replace it with, and click "Replace All".
    - **Break Long Lines**: Click the line break icon, set the max characters per line, and click "Apply Changes". This is useful for improving subtitle readability.
4.  **Export**: Once you are finished, click the **Export** button (top right of the editor) to download your translated subtitle file.

---

## 🔧 Proxy Setup (Optional)

If you are in a region where the Google AI API is blocked or if you encounter network errors (like CORS), you can use a proxy.

1.  **Deploy a Proxy**: You can use the provided [Middleman](https://github.com/yebekhe/middleman) project to deploy your own free proxy on Cloudflare Workers.
2.  **Enable in Fluentify**:
    - Go to **"Advanced Settings"**.
    - Check the **"Use Proxy"** box.
    - The default proxy URL will work, but for better reliability, it's recommended to paste the URL of your own deployed proxy into the **"Custom Proxy URL"** field.

---

## 🛠️ Technology Stack

- **Frontend**: HTML5, Tailwind CSS, Vanilla JavaScript (ES6)
- **AI Engine**: Google Gemini API
- **PDF Processing**: PDF.js by Mozilla

---

## ❤️ Author & Contact

Created with passion by **YEBEKHE**.

- **GitHub**: [@itsyebekhe](https://github.com/itsyebekhe)
- **X (Twitter)**: [@yebekhe](https://x.com/yebekhe)
- **Telegram**: [@yebekhe](https://t.me/yebekhe)

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
