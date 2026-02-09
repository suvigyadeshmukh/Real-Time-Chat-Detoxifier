
---

<div align="center">

# 🛡️ SecondThought
### *Kindness as a Service (KaaS)*

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/downloads/)
[![AI Powered](https://img.shields.io/badge/AI-Sentence--Transformers-orange?style=for-the-badge)](https://www.sbert.net/)
[![Made With Love](https://img.shields.io/badge/Made_with-Love-ff69b4.svg?style=for-the-badge&logo=heart&logoColor=white)](https://github.com/suvigyadeshmukh)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://opensource.org/licenses/MIT)

**SecondThought** isn't just a filter—it's a teacher. Using advanced vector embeddings, it understands the *intent* behind toxicity and suggests constructive alternatives in real-time.

[ View Demo ]( # )  •  [ Report Bug ]( # )  •  [ Request Feature ]( # )

</div>

---

## 🔮 The Magic Behind It

Most filters are dumb; they just block "bad words." **SecondThought** reads between the lines.

1.  **🧠 Semantic Brain**: We use `all-MiniLM-L6-v2` to convert text into 384-dimensional meaning vectors.
2.  **🎭 Context Aware**: A "Gaming" lobby allows trash talk. A "Kids" app allows none. We know the difference.
3.  **✨ Rehabilitation**: Instead of banning users, we offer them a second chance by suggesting a polite rewrite using **Cosine Similarity** search.

---

## ⚡ Features

* **Zero-Shot Toxicity Detection**: Catches sarcasm and slang that keyword lists miss.
* **Ultralow Latency**: Engineered for real-time chat (<50ms response time).
* **Smart Suggestions**: Auto-converts *"You are trash"* → *"I disagree with your playstyle."*
* **Privacy First**: Runs 100% locally. No data is sent to external APIs.

---

## 📊 Adaptive Sensitivity Modes

| Mode | Threshold | Vibe Check |
| :--- | :--- | :--- |
| 🎮 **Gaming** | `0.60` | **High Tolerance.** Allow banter, block hate speech. |
| 📱 **Social** | `0.50` | **Balanced.** Standard community guidelines. |
| 💼 **Professional**| `0.30` | **Strict.** Workplace safe. No aggression allowed. |
| 👶 **Kids** | `0.15` | **Safe Space.** Maximum protection. Positive vibes only. |

---

## 🚀 Getting Started

### 1. Install Dependencies
```bash
pip install numpy pandas scikit-learn sentence-transformers

```

### 2. Run the Engine

```python
# Assuming your file is named second_thought.py
from second_thought import SecondThought

# Initialize (Downloads model on first run automatically)
bot = SecondThought()
bot.load_and_train()

# Check a message
payload = {
    "text": "stop talking you are useless",
    "platform": "kids"
}

result = bot.filter_text(payload)

print(f"Severity: {result['severity']}")       # Output: SEVERE
print(f"Suggestion: {result['correct_text']}") # Output: "Be quiet."

```

## 📚 Data & Acknowledgements

This project stands on the shoulders of giants. We utilize the **ParaDetox** dataset to power our rehabilitation engine.

> **Dataset Source**: [ParaDetox: Parallel Detoxification Dataset](https://github.com/s-nlp/paradetox)
> *Logacheva, V., Dementieva, D., Ustyantsev, S., Moskovskiy, A., Dale, D., Krotova, I., Semenov, N., & Panchenko, A. (2022). ParaDetox: Detoxification with Parallel Data. ACL 2022.*

---
<div align="center">

## 🤝 Contributing

<br>

Contributions, issues, and feature requests are welcome!<br>
Feel free to check the [issues page](https://github.com/suvigyadeshmukh/Real-Time-Chat-Detoxifier/issues).

<br>

<b>Created by <a href="https://github.com/suvigyadeshmukh">Suvigya Deshmukh</a></b>
<br>
<i>Passionate about AI, NLP, and making the internet a kinder place.</i>
<br><br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/suvigyadeshmukh)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/suvigyadeshmukh)

</div>
