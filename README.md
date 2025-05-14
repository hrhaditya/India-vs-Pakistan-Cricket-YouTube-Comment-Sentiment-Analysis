🇮🇳 India vs Pakistan Cricket YouTube Comment Sentiment Analysis 🇵🇰

A multilingual Natural Language Processing (NLP) project aimed at analyzing fan sentiments from YouTube comments during the iconic India vs Pakistan cricket rivalry. This study investigates 15,000+ user comments posted across multiple match highlight videos to uncover emotional trends, shifts in public sentiment, and model performance on code-mixed (Hindi-English) social media data.
🎯 Objective

The goal of this project is to:

    Understand fan sentiment and emotional expression during high-stakes India-Pakistan cricket matches.

    Compare the effectiveness of multilingual and zero-shot models in analyzing code-mixed, unstructured YouTube data.

    Track how sentiment shifts occur in relation to key events (e.g., match start, wickets, final results).

    Evaluate temporal sentiment patterns across time.

📦 Dataset

    Source: Scraped from public YouTube videos featuring match highlights, post-match reviews, and fan reactions.

    Volume: 15,000+ comments

    Language: Predominantly code-mixed Hindi-English, with some pure Hindi and English texts.

🧹 Preprocessing

    Removed emojis, timestamps, and special characters

    Normalized Hindi transliterations and Roman Hindi spellings

    Dropped spam and bot-like content

    Retained only unique, meaningful user inputs for sentiment evaluation

🤖 Models Used
🔹 Google Gemini Pro (Zero-shot)

    Zero-shot sentiment classification using custom prompts

    Scalable and fast, achieved ~87% alignment with ground truth labels

    Great for code-mixed and low-resource language handling

🔹 HingRoBERTa

    Fine-tuned RoBERTa model for Hinglish (code-mixed Hindi-English)

    Strong performance on informal and emotionally charged text

🔹 MuRIL (Multilingual Representations for Indian Languages)

    Trained on 17 Indian languages including Hindi

    Effective for detecting subtle sentiment cues in Romanized Hindi

🔹 CardiffNLP / Twitter RoBERTa

    Used for baseline performance on English-only sentiment classification

    Less effective on code-mixed data, included for comparison

📊 Methodology

    Preprocessing the scraped comments to remove noise and normalize language.

    Model inference using the above models to classify each comment as:

        Positive

        Negative

        Neutral

    Comparative evaluation across models using accuracy and label agreement scores.

    Temporal analysis to observe shifts in sentiment before, during, and after the match.

    Data visualization using matplotlib to plot trends and comparisons.

📈 Key Insights

    💬 Code-mixed models (MuRIL, HingRoBERTa) performed significantly better than English-only baselines in capturing nuanced sentiments.

    📉 Sentiment dips were clearly observed after crucial match events (like losing a wicket or match).

    🧠 Gemini Pro’s zero-shot performance was surprisingly robust, even without domain-specific fine-tuning.

    📆 Temporal analysis helped highlight emotional spikes aligned with match moments (boundaries, innings breaks, results).


🧰 Tech Stack

    Languages: Python

    Libraries: transformers, pandas, matplotlib, google.generativeai, tqdm

    Models: Gemini Pro API, MuRIL, HingRoBERTa, CardiffNLP

isual Results & Analysis
🌤️ Word Cloud Visualizations

To better understand the vocabulary associated with various sentiments, we generated word clouds from model predictions for different sentiment classes:
✅ Gemini Pro – Positive Sentiment

    Most frequent positive terms include: India, love, match, Pakistan, team, Rohit, Sachin

    Indicates strong admiration and emotional connection from both fanbases.

✅ Hing-RoBERTa – Positive Sentiment

    Words like Sachin, team, cup, win, and match are dominant.

    Reflects celebratory expressions and match enthusiasm.

❌ GPT (Zero-Shot) – Negative Sentiment

    Negative words such as commentary, fixed, Akash Chopra, and nahi (no) appear frequently.

    Common fan frustration themes: poor commentary, match-fixing claims, or dissatisfaction with team decisions.

⚪ GPT – Neutral Sentiment

    Neutral conversations feature descriptive terms: match, India, Pakistan, youtube, commentary, watching.

    Often factual or observational in nature, lacking emotional tone.

✅ GPT – Positive Sentiment

    Very similar to Gemini and Hing-RoBERTa, indicating consistent keyword presence across models.

    Prominent terms: Pakistan, India, love, match, best, Shaheen, Dhoni.

📈 Temporal Sentiment Analysis

Temporal trends were mapped to study how comment sentiment evolved over time using timestamps from YouTube metadata.
📆 Gemini Pro – Sentiment Over Time

    Spikes in positive sentiment correspond to major India-Pakistan match events (e.g., 2019 World Cup, 2022 Asia Cup).

    Model also flagged a small proportion of errors during early dataset entries with non-standard text.

📆 Hing-RoBERTa – Sentiment Over Time

    Surprising concentration of negative sentiment spikes around match dates.

    Indicates HingRoBERTa’s higher sensitivity to emotionally charged language in code-mixed text.

🔍 Future Work

    Integrate emotion classification (e.g., joy, anger, surprise) alongside sentiment.

    Expand to other cricket rivalries or sports datasets.

    Fine-tune HingRoBERTa and MuRIL further on sports-comment-specific data.

    Deploy as an interactive dashboard using Streamlit or Dash.
