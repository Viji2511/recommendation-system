# recommendation-system


# AI-Based Internship Recommendation System

## 📌 Overview
This project is a **lightweight AI-powered internship recommender** designed for the PM Internship Scheme.  
It matches candidates to **3–5 most relevant internships** based on skills, interests, and location.

## 🚀 Features
- **User Profile Input:** Education, skills, location, sector interests (with voice input + translation)
- **Preprocessing & NLP:** Skill extraction, language translation, tokenization
- **Filtering & Matching:** Rule-based location filter + ML-light similarity scoring
- **Recommendation Generation:** Top 3–5 internships ranked by match score
- **Explainable Output:** Show matched skills & relevance score in card format
- **Feedback Loop:** Save likes/saves and adapt recommendations

## 🛠️ Tech Stack
- **Python** (Google Colab / Jupyter)
- **Libraries:** pandas, numpy, scikit-learn, sentence-transformers, spacy, rapidfuzz, googletrans, ipywidgets
- **NLP:** spaCy for tokenization & entity extraction, Google Translate for multi-language support
- **Embedding Model:** `all-MiniLM-L6-v2` from SentenceTransformers

## 🧠 Methodology
1. **Load Dataset** – Internshala internship dataset
2. **Clean & Normalize** – Remove duplicates, normalize text
3. **Skill Extraction** – Keyword/NLP based skill tagging
4. **Embedding Generation** – Encode internship titles & companies using transformer embeddings
5. **User Query Parsing** – Translate to English, extract skills, detect location
6. **Filtering & Scoring** – Rule-based filtering + weighted similarity scoring
7. **Recommendation Display** – Show 3–5 internships with matched skills and scores
8. **Feedback Capture** – Store user likes/saves for future personalization

## 📂 Project Structure
```
├── internship companies.csv      # Raw dataset
├── internships_with_skills.csv   # Processed dataset with skills
├── corpus_embeddings.npy         # Saved embeddings
├── feedback.csv                  # User feedback log
├── recommendation_system.ipynb   # Main Colab notebook
└── README.md                     # Project documentation
```

## ▶️ How to Run
1. Open `recommendation_system.ipynb` in **Google Colab**
2. Run setup cells to install dependencies
3. Run data preprocessing cells to clean and extract skills
4. Generate embeddings (only first time)
5. Enter a query in natural language (or use mic button)
6. Run recommendation cell → Top 3–5 internships displayed as cards
7. (Optional) Save feedback to improve personalization

## 🧩 Example Query
```
"work from home python machine learning internship"
```
**Output:** 3–5 internship cards with matched skills and relevance score.

## 📊 Evaluation
- **Precision@3:** Manually check relevance of top-3 suggestions
- **User Feedback:** Log likes/saves to fine-tune recommendations

## 🌱 Future Improvements
- More advanced skill extraction (NER + deep learning)
- Use AI4Bharat translation models for better Indic language support
- Deploy as a microservice for integration with PM Internship Portal
