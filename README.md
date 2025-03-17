news-summarization-tts
News Summarization &amp; Hindi TTS Application A web-based tool that extracts news articles about a given company, performs sentiment analysis, conducts comparative analysis, and generates Hindi text-to-speech (TTS) output.

News Summarization & Hindi Text-to-Speech (TTS) Application

Project Overview
This project extracts news articles related to a given company, performs sentiment analysis, conducts a comparative analysis, and converts the summarized content into Hindi speech. The web-based application allows users to enter a company name and receive a structured sentiment report along with an audio output.

 #Features
- Web Scraping: Extracts at least 10 unique news articles using `BeautifulSoup`.
- Sentiment Analysis: Categorizes articles as Positive, Negative, or Neutral.
- Comparative Analysis: Highlights differences in sentiment across multiple articles.
- Hindi Text-to-Speech (TTS): Converts summary to Hindi audio using `gTTS`.
- API Integration: Allows seamless frontend-backend communication.
- User Interface: Built using `Streamlit` for interactive input.
- Deployment: Hosted on Hugging Face Spaces.


# Installation

# Install Dependencies
```bash
pip install -r requirements.txt
```

# Run the Flask API
```bash
python app.py
```

# Run the Streamlit Frontend
```bash
streamlit run app.py
```

# API Endpoints
# Fetch News Articles
**Endpoint:** `GET /news?company=Tesla`

# Response:
```json
{
  "company": "Tesla",
  "articles": [
    {
      "title": "Tesla's New Model Breaks Sales Records",
      "link": "https://news.example.com/tesla-sales"
    }
  ]
}
```

# Sentiment Analysis
Endpoint: `POST /sentiment`

**Request:
```json
{
  "text": "Tesla's stock rose 10% after the new launch."
}
```

Response:
```json
{
  "sentiment": "Positive"
}
```

# Generate Hindi TTS
Endpoint:`POST /tts`

Request:
```json
{
  "text": "टेस्ला ने अपनी नई मॉडल लॉन्च की।"
}
```

Response:
```json
{
  "audio_file": "output.mp3"
}
```

# Comparative Sentiment Analysis
**Endpoint:** `POST /comparative_sentiment`

Request:
```json
{
  "sentiments": ["Positive", "Negative", "Neutral"]
}
```

Response:
```json
{
  "comparative_sentiment": "Neutral"
}
```

Output Format
```json
{
  "Company": "Tesla",
  "Articles": [
    {
      "Title": "Tesla's New Model Breaks Sales Records",
      "Summary": "Tesla's latest EV sees record sales in Q3...",
      "Sentiment": "Positive",
      "Topics": ["Electric Vehicles", "Stock Market", "Innovation"]
    },
    {
      "Title": "Regulatory Scrutiny on Tesla's Self-Driving Tech",
      "Summary": "Regulators have raised concerns over Tesla’s self-driving software...",
      "Sentiment": "Negative",
      "Topics": ["Regulations", "Autonomous Vehicles"]
    }
  ],
  "Comparative Sentiment Score": {
    "Sentiment Distribution": {
      "Positive": 1,
      "Negative": 1,
      "Neutral": 0
    },
    "Coverage Differences": [
      {
        "Comparison": "Article 1 highlights Tesla's strong sales, while Article 2 discusses regulatory issues.",
        "Impact": "The first article boosts confidence in Tesla's market growth, while the second raises concerns about future regulatory hurdles."
      }
    ],
    "Topic Overlap": {
      "Common Topics": ["Electric Vehicles"],
      "Unique Topics in Article 1": ["Stock Market", "Innovation"],
      "Unique Topics in Article 2": ["Regulations", "Autonomous Vehicles"]
    }
  },
  "Final Sentiment Analysis": "Tesla’s latest news coverage is mostly positive. Potential stock growth expected.",
  "Audio": "[Play Hindi Speech]"
}
```

# Deployment on Hugging Face Spaces
1. Create a new Hugging Face Space ([Create Here](https://huggingface.co/spaces)).
2. Choose **Streamlit** as the SDK.
3. Push the repository to Hugging Face.
4. Run the application and share the deployment link.

# Documentation Requirements
- Project Setup: Steps to install and run the application.
- Model Details: Explanation of models used for summarization, sentiment analysis, and TTS.
- API Development: Description of API endpoints and usage.
- Third-Party APIs: Mention any external APIs used and how they are integrated.
- Assumptions & Limitations: Any constraints or assumptions made during implementation.








 
