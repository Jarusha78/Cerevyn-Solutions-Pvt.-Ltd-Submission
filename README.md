
# 🤖 AI-Powered Customer Support Conversational Assistant

An intelligent conversational chatbot designed for **e-commerce customer support**.
The system understands natural language queries and provides accurate responses about products such as **price, discounts, stock availability, and product details** using NLP techniques and an optional LLM (ChatGPT) interface.

---

## 📌 Introduction
With the rapid growth of online shopping, customers expect **instant responses** to their queries.  
Traditional rule-based chatbots fail to handle follow-up questions and contextual conversations.

This project solves that problem by creating a **context-aware AI chatbot** capable of:
- Understanding natural language
- Handling follow-up queries
- Providing polite fallback responses
- Returning reliable domain-specific answers

---

## 🎯 Objectives
- Build a customer support chatbot for e-commerce platforms
- Understand user queries in natural language
- Maintain conversation context
- Provide accurate responses without hallucinations
- Demonstrate practical NLP + Conversational AI implementation

---

## 🧠 How the System Works

### 1. Data Collection
- Product data scraped from e-commerce websites (Shopify collections)
- Stored in CSV format

### 2. Text Preprocessing
- Text cleaning
- Stopword removal
- Lemmatization
- Extractive summarization

### 3. Intent Detection
Queries are classified into:
- Price
- Discount
- Stock availability
- Product details
- General information

### 4. Information Retrieval
- TF-IDF Vectorization
- Cosine Similarity Matching

### 5. Response Generation
- Rule-based NLP for correctness
- Optional ChatGPT integration for fluent replies

### 6. Conversation Handling
- Session memory maintains context for follow-up queries

---

## 🏗️ Tech Stack

### Programming Language
- Python 3.x

### Libraries & Frameworks
- Flask (API backend)
- Flask-SocketIO (real-time communication)
- NLTK (text preprocessing)
- Scikit-learn (TF-IDF & cosine similarity)
- Pandas & NumPy (data processing)
- BeautifulSoup & Requests (web scraping)
- Schedule & Threading (background jobs)
- OpenAI API (optional ChatGPT integration)

---

## ✨ Key Features

### FAQ Answering
The bot can answer:
- “What is the price?”
- “Is it in stock?”
- “What discount is available?”

### Follow-Up Question Handling
Remembers previous product context:
- “What about discount?”
- “Is it available?”
- “Tell me more details”

### Polite Fallback Responses
Handles irrelevant queries gracefully without crashing.

### Hybrid NLP + LLM
- NLP → accuracy
- LLM → natural conversation

---

## 🔌 API Design

### WebSocket Events
| Event | Description |
|------|------|
| `run-scrape` | Scrapes product data |
| `query_with_inputs` | User asks a question |
| `reset_session` | Clears conversation memory |
| `health` | Server status check |

Backend: **Flask + WebSocket API**

---

## ⚠️ Error Handling
- Invalid URLs rejected safely
- Empty datasets handled
- Low similarity queries trigger fallback
- Session reset supported

---

## 🚧 Limitations
- Text-based only (no voice support)
- Depends on dataset quality
- LLM requires internet + API key

---

## 🚀 Future Improvements
- Voice assistant integration
- Multilingual chatbot
- Deep-learning intent classification
- React-based web UI
- Analytics dashboard

---

## 🧪 Example Use Cases
- E-commerce websites
- Online product catalogues
- Customer service automation
- FAQ automation systems

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
python app.py
```

---

## ▶️ Running the Server

```bash
python app.py
```

Server will start on:
```
http://localhost:5000
```

---

## 💬 Example Queries
```
What is the price of this product?
Is it available?
Any discount?
Tell me more details.
```

---

## 📊 Conclusion
This project demonstrates a practical implementation of a real-world conversational AI system combining NLP techniques with optional LLM support.  
It provides accurate, context-aware responses and shows how AI can automate customer support effectively.
