# 🏡 HomeMatch – Personalized Real Estate Gen AI Agent

Welcome to **HomeMatch**, an intelligent real estate application developed for **Future Homes Realty**. This app reimagines how buyers discover their dream homes by providing **personalized property listings** tailored to each buyer’s unique preferences.

## 📌 Project Overview

In a market where personalization is key, HomeMatch leverages **Large Language Models (LLMs)** and **vector databases** to transform conventional listings into customized narratives that speak directly to buyers. From architectural styles to lifestyle needs, HomeMatch delivers listings that feel handpicked.

---

## 🚀 Key Features

### 🔍 Capturing Buyer Preferences
Buyers can specify:
- Location  
- Property type  
- Budget  
- Desired amenities  
- Lifestyle choices  

These inputs are interpreted via LLMs to extract nuanced preferences beyond basic filters.

### 🧠 Vector Database Integration
- Uses **ChromaDB** (or any vector store) to embed and store real estate listings.
- Listings are semantically searchable using buyer preferences.
- Matches consider neighborhood vibes, home features, and lifestyle alignment.

### ✍️ Personalized Property Descriptions
- Tailored descriptions highlight buyer-relevant features.
- Powered by LLMs, each listing is rewritten to speak to the buyer—without altering factual details.

### 🏘️ Personalized Listings Output
- Final listings are presented in natural, narrative-rich formats tailored to the buyer’s interests.

---

## 🛠️ Project Steps

### 1. Setup
- Initialize a Python project.
- Create and activate a virtual environment.
- Install dependencies:

```bash
pip install -r requirements.txt
```

**Dependencies** (in `requirements.txt`):
```
langchain
openai  # or another LLM provider
chromadb  # or lancedb
tqdm
dotenv
```

### 2. Generate Sample Property Listings
Use LLMs to generate 10+ diverse listings for development/testing. Example:

```python
{
  "Neighborhood": "Green Oaks",
  "Price": 800000,
  "Bedrooms": 3,
  "Bathrooms": 2,
  "Size": "2,000 sqft",
  "Description": "...",
  "Neighborhood_Description": "..."
}
```

### 3. Store Listings in Vector Database
- Configure **ChromaDB** or **LanceDB**.
- Embed listings using a text embedding model.
- Store vectors and metadata for semantic search.

### 4. Build Buyer Preferences Interface
Ask questions such as:

```python
questions = [
  "What size house are you looking for?",
  "Top 3 priorities?",
  "Most valued amenities?",
  "Preferred transportation options?",
  "Suburban or urban?"
]
```

Parse responses into a structured preference profile.

### 5. Perform Semantic Search
- Run queries against vector DB using embeddings of buyer preferences.
- Retrieve and rank matching listings.

### 6. Personalize Descriptions
- Use LLMs to rewrite each matched listing.
- Highlight features that matter most to the buyer.

---

## 🔮 Future Improvements
- Add a UI for buyer interactions.
- Integrate geolocation and map visualizations.
- Feedback loop to improve personalization quality.
- Multi-language support for diverse users.

---

## 🤝 Contributing
Contributions, suggestions, and feedback are welcome! Open an issue or submit a pull request to enhance functionality.

---

## 📃 License
This project is licensed under the [MIT License](LICENSE).
