# 🎓 CampusGuide Hyderabad — AI Campus Info Chatbot

An AI-powered chatbot for answering questions about colleges in Hyderabad, Telangana. Built for the Capabl Track A project.

---

## 🏛️ Colleges Covered

| College | Location | Type |
|--------|----------|------|
| JNTU Hyderabad | Kukatpally | University |
| Osmania University | Amberpet | University |
| CBIT | Gandipet | Engineering |
| IIIT Hyderabad | Gachibowli | Deemed University |
| NIT Warangal | Warangal | NIT |
| ISB Hyderabad | Gachibowli | Business School |
| NALSAR University | Shameerpet | Law University |
| University of Hyderabad | Gachibowli | Central University |
| VNR VJIET | Bachupally | Engineering |
| Vasavi College | Ibrahimbagh | Engineering |
| Nizam College | Basheerbagh | Arts & Science |
| MVSR Engineering | Nadergul | Engineering |
| Muffakham Jah | Banjara Hills | Engineering |
| VJIT | Bachupally | Engineering |
| St. Francis College | Begumpet | Women's College |

---

## ⚙️ Tech Stack

- **Frontend:** Streamlit with custom CSS
- **Backend:** Python
- **LLM:** Groq API (free) — `llama-3.3-70b-versatile`
- **Scraping:** BeautifulSoup + requests
- **Data:** Scraped live from official college websites + local cache

---

## 🚀 Setup Instructions

### Step 1 — Clone & enter folder
```bash
git clone <your-repo-url>
cd campus_chatbot
```

### Step 2 — Create virtual environment
```bash
python -m venv venv

# Windows:
venv\Scripts\activate

# Mac/Linux:
source venv/bin/activate
```

### Step 3 — Install dependencies
```bash
python -m pip install -r requirements.txt
python -m pip install groq
```

### Step 4 — Get a free Groq API key
1. Go to https://console.groq.com
2. Sign up for free with your Gmail
3. Click **API Keys** → **Create API Key**
4. Copy the key

### Step 5 — Configure API key
Create a `.env` file in the project folder and add:
```
GROQ_API_KEY=gsk_your_key_here
```

### Step 6 — Run the app
```bash
python -m streamlit run app.py
```

The app opens at **http://localhost:8501**

---

## 📖 Usage Guide

1. Open the app at http://localhost:8501
2. Ask questions in the chat box. Examples:
   - *"What are the B.Tech fees at CBIT?"*
   - *"How do I apply to JNTU Hyderabad?"*
   - *"Tell me about placements at Vasavi College"*
   - *"Which college is best for CSE in Hyderabad?"*
   - *"What is EAMCET and how does it work?"*

---

## 📁 Project Structure

```
campus_chatbot/
├── app.py                  # Main Streamlit UI
├── chatbot.py              # Groq LLM chatbot logic
├── scraper.py              # BeautifulSoup web scraper
├── colleges_config.py      # College URLs and metadata
├── requirements.txt        # Python dependencies
├── .env                    # Your API key (don't commit!)
├── .gitignore              # Ignores .env, venv, cache
└── data/
    └── scraped_cache.json  # Cached college website content
```

---

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| `ModuleNotFoundError: groq` | Run `python -m pip install groq` |
| `streamlit not recognized` | Use `python -m streamlit run app.py` |
| `GROQ_API_KEY not found` | Check your `.env` file has the key with no spaces |
| Scraping fails for a college | Website may be down; cached data is used automatically |
| `cannot import name 'init_gemini'` | Make sure you have the latest `app.py` from the repo |

---

## 📦 Deployment (Streamlit Cloud)

1. Push code to GitHub (`.env` is in `.gitignore` so it won't be uploaded)
2. Go to https://share.streamlit.io
3. Connect your GitHub repo
4. Go to **App settings → Secrets** and add:
```
GROQ_API_KEY = "gsk_your_key_here"
```
5. Deploy!

---

## 🎯 Assessment Checklist (Track A)

- [x] GitHub repo with project structure
- [x] Python + Streamlit + BeautifulSoup
- [x] Web scraping for college websites
- [x] Campus info categorization (location, fees, admissions, placements)
- [x] Streamlit chatbot interface
- [x] Free LLM via Groq API (no quota issues)
- [x] Conversation memory (last 2 exchanges)
- [x] Contact info, location, and facility details
- [x] Deployable on Streamlit Cloud

---

Built as part of **Capabl Interactive Campus Info Chatbot Project — Track A**
