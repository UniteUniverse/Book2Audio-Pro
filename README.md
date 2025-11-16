# 🌟 Book2Audio Pro — Convert Any Book into Studio-Quality Audio (Fully Automated)

Book2Audio Pro is a next-level n8n automation workflow that transforms any uploaded PDF book into chapter-wise AI-generated audio files—neatly chunked, named, and uploaded straight to your Google Drive.  
No coding. No manual splitting. Just upload → chill → get audio. 🎧🔥

---

## 🚀 What This Workflow Actually Does

This workflow isn’t just another PDF-to-audio tool—it’s a **smart pipeline with automation sauce**:

1. **Upload Your Book**  
   A clean n8n Form Trigger lets users upload a PDF file.

2. **Google Drive Folder Auto-Creation**  
   Creates a dedicated folder using the book’s filename for organized outputs.

3. **Extract Text from PDF**  
   Utilizes the Extract From File node to pull out the full text cleanly.

4. **AI Content Structuring (Magic Happens Here ✨)**  
   - Removes Table of Contents  
   - Detects chapters (Roman numerals: CHAPTER I., II., III…)  
   - Auto-splits each chapter into OpenAI-friendly chunks (max 3900 chars)  
   - Creates Netflix-level filenames:  
     `chapter-01-part-01-the-beginning.mp3`

5. **Turn Text → Audio (OpenAI TTS Pro Mode)**  
   Each chunk goes to OpenAI TTS for studio-quality audio generation.

6. **Upload Audio Back to Google Drive**  
   Every generated MP3 automatically lands in the created folder.

7. **Loop Magic**  
   The workflow loops through all chunked items until all audio files are generated and uploaded.

---

## 💡 Why This Workflow Slaps (Gen-Z Approved)

- 🧠 Fully automated—upload once, get everything done  
- 🎧 Podcast-level audio via OpenAI TTS  
- 📚 Perfect for long PDFs (auto chunking is elite)  
- 🔍 Smart chapter detection using regex + Roman numerals  
- 🗂 Organized output—every file is properly named  
- ☁️ Uploads straight to Google Drive

> This is literally the “Spotify for your own PDFs” (but DIY edition 😎).

---

## 🔧 Tech Stack & Nodes Used

- **PurposeNode**
- **User File Upload**
- **Form Trigger**
- **PDF Text Extraction**  
  Extract From File
- **Folder Creation**  
  Google Drive
- **Content Structuring**  
  Custom JavaScript Code Node
- **AI Audio Generation**  
  OpenAI TTS via LangChain Node
- **Looping**  
  Split In Batches
- **Uploading MP3 Files**  
  Google Drive
- **SQL Merge**  
  Merge Node (combineBySql)

---

## 🛠 Setup Instructions

1. **Clone this repo**
git clone https://github.com/UniteUniverse/Book2Audio-Pro

2. **Import the .json workflow into n8n**  
Go to Settings → Import Workflow → Upload File

3. **Add your credentials**  
- Google Drive OAuth2  
- OpenAI API Key

4. **Publish the workflow**  
Set the Form Trigger URL in your browser and start converting books!

---

## 📦 Workflow File

The exported workflow is inside:  
`Book2Audio Pro.json`  
Just import & run.

---

## 🔥 Demo Flow (In Simple Words)

Upload PDF → Extract Text → Clean & Split Chapters → Generate Audio → Upload to Drive → Done.  
Like magic, but automation-powered 🪄⚡

---

## 🧑‍💻 Author

Built with ❤️ & caffeine by **Pratyush Kumar Jha**  
Generative AI Developer • Automation Engineer • n8n Wizard

---

## ⭐ Support the Project

If you vibe with this workflow, give the repo a star 🌟  
It keeps me motivated to ship more automation goodness.
