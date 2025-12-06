# 💬 Streamlit + LangChain Chatbot  
A lightweight chatbot built using **Streamlit** for the frontend and **LangChain + Groq** for ultra-fast LLM inference.  
Includes sentiment analysis, session-based chat memory, and local JSON conversation logging.

[![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://chatbot-template.streamlit.app/)

---

## 🚀 Features

- Interactive chat UI using Streamlit  
- Groq LLM (**llama-3.1-8b-instant**) integration via LangChain  
- **Sentiment analysis** for each user message  
- **Overall conversation sentiment** insights  
- **Advanced emotional interpretation using LLM**  
- JSON-based conversation saving  
- Session-based memory using Streamlit  
- Secure API key loading via `.env`  
- Ultra-fast inference with Groq

---

### TO RUN THE APPLICATION
1.  **Clone the repository:**
    ```bash
    git clone [Your-Repo-URL]
    cd flowstate-talent
    ```
2.  **Install dependencies:*
    ```bash
    pip install -r requirements.txt
    ```
3. **To RUN
    ```bash
    .venv\Scripts\python.exe -m streamlit run streamlit_langchain_app.py --server.port=8508
    ```


## 🧠 Sentiment Analysis (Full Breakdown)

### 🔹 1. **User Message Sentiment (Simple)**
For every message the user sends:

- TextBlob computes **polarity score** (range: -1.0 → +1.0)
- Determines sentiment:
  | Polarity Range | Label |
  |----------------|--------|
  | `> +0.1` |  Positive |
  | `< -0.1` |  Negative |
  | `-0.1 to +0.1` |  Neutral |

📌 **Displayed directly under each user message in the chat UI**

---

### 🔹 2. **Overall Conversation Sentiment (Advanced)**
All user + bot messages are combined to evaluate:

| Metric | Meaning | Range |
|--------|---------|--------|
| Polarity | Emotional tone | -1 (negative) → +1 (positive) |
| Subjectivity | Facts vs opinions | 0 (objective) → 1 (subjective) |

Final sentiment:
| Polarity | Sentiment |
|---------|-----------|
| `> +0.1` |  Positive |
| `< -0.1` |  Negative |
| `-0.1 to +0.1` |  Neutral |

---

### 🔹 3. **Detailed Emotional Analysis (LLM-Powered)**
When available, the chatbot uses the **Groq LLM** to provide:

- Human-style emotional summary
- Emotional trajectory over time
- Tone and psychological shift in the conversation

If the LLM analysis fails, it gracefully falls back to polarity + subjectivity scores.

---

### 💡 Quick Examples
| User Message | Result |
|-------------|--------|
| “I love this!” | Positive |
| “This is terrible.” | Negative |
| “The weather is cloudy.” | Neutral |
| Multiple happy messages across chat | Overall: Positive |

---

## 🧰 Technologies Used

| Layer | Tools |
|-------|-------|
| Frontend | Streamlit |
| Backend / AI | LangChain, Groq API |
| LLM | llama-3.1-8b-instant |
| NLP | TextBlob |
| Utilities | python-dotenv |
| Language | Python 3.13 |

---

## IMPLEMENTED FULL TIER 2

### SCREENSHOTS OF CHATBOT
## showing chats
<img width="1848" height="981" alt="Screenshot 2025-12-06 195337" src="https://github.com/user-attachments/assets/9853556b-9156-4d30-8587-d893fa3e03b6" />

## showing overall sentiments
<img width="1840" height="983" alt="Screenshot 2025-12-06 195403" src="https://github.com/user-attachments/assets/e460226a-3040-4dd1-9d01-b938099abcc0" />

## ADITIONAL FEATURES
### I had added the feature of save that if user want to save the **conversation** the he do, otherwise it does not default get save.
### I had added the feature of **preview** that if user want to check the previous conversation and don't want to load in the conversation then he can use preview
### section where user can preview the conversation in the side bar.


