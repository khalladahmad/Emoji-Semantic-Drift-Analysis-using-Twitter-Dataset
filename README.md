
# 📊 Emoji Semantic Drift Analysis

## 📝 Overview

Do emojis mean the same thing today as they did yesterday? This project explores **Semantic Drift**—the way the meaning and context of emojis evolve over time. By using **Twitter embeddings** and **Cosine Similarity**, we measure how the "contextual fingerprint" of 42 popular emojis changes between simulated time slices (2024–2025).

## 🚀 Key Features

  * **Vectorized Meaning:** Uses Sentence Embeddings to turn tweets into mathematical vectors.
  * **Drift Quantification:** Employs Cosine Similarity to detect shifts in usage.
  * **Large Scale:** Analyzes over **734,286 unique tweets**.
  * **Comparative Study:** Categorizes emojis by their stability (e.g., "Stable" vs. "Emotion-Heavy").

-----

## 🛠️ Methodology

1.  **Preprocessing:** Cleaned and merged 43 emoji-specific CSV files from the Kaggle Twitter Emoji Sentiment dataset.
2.  **Time Slicing:** Created simulated intervals for **2024** and **2025**.
3.  **Embedding:** Computed average sentence embeddings for each emoji per time slice.
4.  **Similarity Check:** Calculated drift using the formula:
    $$Drift = \text{cosine}(t_1, t_2)$$
      * *Lower similarity indicates higher semantic drift.*

-----

## 📈 Key Findings

| Category | Similarity Range | Examples | Characteristics |
| :--- | :--- | :--- | :--- |
| **Highly Stable** | $0.86 - 0.87$ | ❤️ 👍 😂 😎 | Consistent, universal meanings. |
| **Emotion-Heavy** | $0.85 - 0.86$ | 😭 🥹 🥲 🫠 | Nuance depends on user mood. |
| **Moderately Variable** | $0.84 - 0.85$ | 🤡 🖕 💩 😡 | High use in sarcasm/diverse contexts. |

**The Bottom Line:** While most emojis show high stability, "Slang" and "Emotion" emojis are the most likely to shift in meaning based on cultural trends.

-----

## ⚠️ Limitations & Future Work

  * **Simulated Data:** The current drift is based on artificial time slices. Future iterations will use real temporal data (e.g., 2020–2026).
  * **Compute Power:** Planned upgrades include using higher-compute GPUs for deeper Transformer-based models.
  * **Real-time Scrapes:** Future integration with the Twitter (X) API for high-quality, live data.
-----

