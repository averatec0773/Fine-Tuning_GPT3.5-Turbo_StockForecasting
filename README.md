# FineTune_GPT3.5Turbo_StockForecasting

This project explores the fine-tuning of OpenAI’s GPT-3.5 Turbo model for stock price forecasting by integrating **time-series stock data** and **news headlines**. Experiments on the **Bigdata22** and **CIKM18** datasets show that fine-tuning significantly improves the model’s ability to produce accurate and structured predictions. However, its performance still lags behind traditional financial forecasting models, emphasizing the importance of domain-specific optimization in financial NLP tasks.

---

## 📄 Related Paper

**The Limits of Excellence: Assessing Fine-tuned ChatGPT’s Efficacy in Stock Price Forecasting**  
[📄 View Full Paper (PDF)](./The%20Limits%20of%20Excellence%20Assessing%20Fine-tuned%20ChatGPT%E2%80%99s%20Efficacy%20in%20Stock%20Price%20Forecasting.pdf)

---

## 📁 Datasets

Two benchmark financial datasets were used:

- **Bigdata22**: Real-world U.S. stock price data and tweet-based sentiment signals
- **CIKM18**: A more complex financial dataset with longer text and higher noise

Each dataset includes:
- Daily open, high, low, close, adjusted close prices
- Moving averages over 5–30 days
- Chronologically split into training, validation, and testing sets

---

## 🧠 Method Overview

- **Model**: GPT-3.5 Turbo (fine-tuned via OpenAI API)
- **Task**: Predict whether a stock’s price will **Rise** or **Fall** the next day
- **Input Format**: Time-series price data + headline/news context
- **Prompt Design**: Structured questions like:


- **Fine-Tuning Setup**: 2 epochs, structured JSONL prompts

---

## 📊 Results Visualization

### 📈 F1 Score Comparison
![F1 Score Chart](results/result1.png)

### 📉 Model Accuracy Over Epochs
![Accuracy Chart](results/result2.png)

- On **Bigdata22**: F1 improved from `0.4310` (base) to `0.8336` (fine-tuned)
- On **CIKM18**: Accuracy improved from `0.1601` to `0.4987`
- Fine-tuned models produced concise predictions ("Rise"/"Fall"), unlike the verbose outputs of the original
