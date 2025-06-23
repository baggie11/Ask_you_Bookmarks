# 🔖 Bookmark AI — Smarter Search for Your Saved Links

Tired of saving hundreds of bookmarks and forgetting why you saved them in the first place?  
**Bookmark AI** lets you semantically search through your Chrome bookmarks using natural language — not just keywords or page titles!

---

## 🌟 Features

- ✅ **One-click semantic search** over your saved bookmarks  
- 🔍 Powered by **Google Gemini embeddings** and **FAISS vector search**
- 📚 Extracts **real content** from bookmarked pages (not just titles)
- 🧠 Understands your questions even if you forgot the exact wording
- 🗂️ Works across **all folders** in your Chrome bookmarks
- ⚡ FastAPI backend with Chrome Extension frontend

---

## 🧠 How It Works

1. **Fetches** your saved Chrome bookmarks
2. **Scrapes** the content + titles of each URL using `BeautifulSoup`
3. **Embeds** that text using `GoogleGenerativeAIEmbeddings`
4. **Stores** them in a local FAISS vector database
5. You can now **ask natural questions**, and get relevant bookmark links — even if the title doesn't match exactly!

---

## 🛠️ Tech Stack

- **Chrome Extension (Frontend)**
  - JavaScript
  - Bookmark API
  - Semantic UI & DOM rendering

- **Backend**
  - Python + FastAPI
  - `httpx`, `BeautifulSoup`
  - `langchain`, `FAISS`, `GoogleGenerativeAIEmbeddings`

---

## 📦 Setup Instructions

### 🔌 Backend

```bash
# Clone the repo
git clone https://github.com/your-username/bookmark-ai.git
cd bookmark-ai/backend

# Install dependencies
pip install -r requirements.txt

Note: Use your Gemini API key by pasting it in app.py:

# Run the FastAPI server
uvicorn app:app --reload
