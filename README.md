# 📚 BookBug – AI Book Recommendation Assistant

BookBug is an AI-powered book recommendation assistant that helps users discover, understand, and continue their reading journey.

Users can **upload a photo of their bookshelf or enter book names/text**, and BookBug uses AI to identify and understand the books, provide summaries, explain their main topics, and recommend the next books that logically continue the user's learning path or syllabus.

The application can also generate a **WhatsApp-friendly summary** of the books discussed and send it directly to the user's WhatsApp.

## ✨ Features

* 📸 **Book Image Analysis**
  Upload a photo of your bookshelf and let the AI analyze the books.

* 📖 **Book Understanding**
  Identify books and provide information about their language, subject, and main topics.

* 📝 **Book Summaries**
  Get short and useful summaries of the books discussed.

* 📚 **Learning Path Recommendations**
  Get recommendations for the next books based on the topics and syllabus of the current books.

* 🔮 **Future Book Suggestions**
  Discover additional books that can help continue your learning journey.

* 🌐 **Language-Aware Recommendations**
  Recommendations consider the language of the books being discussed.

* 💬 **Conversational AI**
  Chat naturally with the AI assistant about books and reading.

* 📱 **WhatsApp Summary**
  Generate a concise summary of the conversation and send it to WhatsApp.

## 🛠️ Tech Stack

| Technology           | Purpose                                      |
| -------------------- | -------------------------------------------- |
| **Python**           | Application development                      |
| **Streamlit**        | Interactive web interface                    |
| **Google Gemini**    | AI-powered book analysis and recommendations |
| **Google GenAI SDK** | Communication with Gemini                    |
| **Twilio**           | WhatsApp messaging                           |
| **Git & GitHub**     | Version control and project hosting          |

## 🏗️ Project Structure

```text
Book-bug/
│
├── app.py
├── prompts.py
├── requirements.txt
├── .gitignore
│
└── .streamlit/
    └── secrets.toml
```

### `app.py`

The main Streamlit application.

It handles:

* User onboarding
* Name and WhatsApp number collection
* Chat interface
* Book image uploads
* Text-based book input
* Gemini API communication
* Conversation management
* WhatsApp summary generation
* Twilio WhatsApp messaging

### `prompts.py`

Contains the AI instructions used by BookBug.

It includes:

* System prompt
* Welcome message
* WhatsApp summary prompt

The system prompt keeps the assistant focused on books, reading, studying, and book recommendations.

### `requirements.txt`

Contains the main Python dependencies:

```text
google-genai
streamlit
twilio
```

## 🔄 How BookBug Works

```text
User
  │
  ├── Uploads bookshelf image
  │        OR
  └── Enters book names/text
           │
           ▼
     Streamlit Interface
           │
           ▼
      Google Gemini AI
           │
           ├── Identifies books
           ├── Understands topics
           ├── Summarizes books
           └── Recommends next books
           │
           ▼
      Book Recommendations
           │
           ▼
    WhatsApp Summary
           │
           ▼
         Twilio
           │
           ▼
      User's WhatsApp
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/sowmya-varvala/Book-bug.git
```

### 2. Navigate to the project

```bash
cd Book-bug
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

**Windows PowerShell:**

```powershell
venv\Scripts\Activate.ps1
```

**Windows CMD:**

```cmd
venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure API credentials

Create:

```text
.streamlit/secrets.toml
```

Add the required credentials:

```toml
GEMINI_API_KEY = "your_gemini_api_key"

TWILIO_ACCOUNT_SID = "your_twilio_account_sid"
TWILIO_AUTH_TOKEN = "your_twilio_auth_token"
TWILIO_WHATSAPP_FROM = "your_twilio_whatsapp_number"
TWILIO_CONTENT_SID = "your_twilio_content_sid"
```

**Do not commit `secrets.toml` to GitHub.** Keep API keys and authentication credentials private.

### 7. Run the application

```bash
streamlit run app.py
```

The application will open in your browser.

## 💡 Example Usage

1. Enter your name.
2. Enter your WhatsApp number with the country code.
3. Start the BookBug chat.
4. Upload a photo of your bookshelf or enter book names.
5. Ask BookBug about the books.
6. Get summaries and topic information.
7. Receive recommendations for the next books in your learning path.
8. Click **Send to WhatsApp** to receive a summary of your discussion.

## 🎯 Project Objective

The main objective of BookBug is to make book discovery and continuous learning easier by combining:

* Artificial Intelligence
* Image understanding
* Conversational interfaces
* Personalized recommendations
* Learning-path progression
* WhatsApp communication

Instead of simply recommending random books, BookBug focuses on **what the user is currently learning and what they should read next**.

## 🔮 Future Enhancements

Possible future improvements include:

* 🔎 More accurate book title and author recognition
* 📚 Personalized reading history
* ⭐ Book ratings and reviews
* 👤 User profiles
* 🗂️ Personal digital bookshelf
* 🌍 Support for more languages
* 🎯 More advanced personalized recommendation algorithms
* 📊 Reading progress tracking
* 🔗 Book purchase/library links
* ☁️ Cloud deployment
* 💾 Database integration for storing user preferences and reading history

## 👩‍💻 Author

**Sowmya Varvala**

B.Tech – Computer Science and Engineering

GitHub:
https://github.com/sowmya-varvala

---

⭐ If you find this project interesting, feel free to explore the repository and try BookBug!
