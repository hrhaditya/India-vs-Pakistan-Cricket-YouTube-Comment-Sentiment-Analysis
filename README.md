# India-vs-Pakistan-Cricket-YouTube-Comment-Sentiment-Analysis

A multilingual sentiment analysis project exploring YouTube fan comments on India vs Pakistan cricket matches. Analyzed 15,000+ comments using Hindi-English (code-mixed) capable models like MuRIL, HingRoBERTa, and Gemini Pro to study public sentiment, emotion trends, and temporal behavior.
🔍 Key Features

    Preprocessing of 15K+ multilingual YouTube comments

    Sentiment classification with:

        🤖 Google Gemini Pro (Zero-shot)

        📚 HingRoBERTa

        🌍 MuRIL

    Performance comparison across models

    Time-series sentiment trends

    Visualized results with Matplotlib

🧰 Tech Stack

    Python, pandas, transformers, Google GenerativeAI, matplotlib

    Models used: cardiffnlp/twitter-roberta-base, HingRoBERTa, MuRIL, Gemini Pro

📊 Results

    Gemini Pro achieved ~87% agreement with ground truth sentiment.

    Code-mixed models outperformed English-only baselines.

    Notable shifts in sentiment before/after match events.
