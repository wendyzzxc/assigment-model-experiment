Problem Statement
Membandingkan pendekatan klasik Machine Learning (Scikit-learn) dan LLM API (Gemini) untuk sentiment analysis
ulasan pelanggan e-commerce (positif/negatif). Tujuan: memberikan rekomendasi pendekatan terbaik untuk produksi.

Dataset

- File: `data/customer_reviews_sentiment.csv`
- 200 baris, kolom: `review_id`, `product_name`, `review_text`, `sentiment`

Eksperimen

1. **Model Klasik:** TF-IDF (n-gram 1-2) + Logistic Regression.
2. **LLM API:** Gemini 3.5 Flash Lite dengan few-shot promptin, temperature=0.2

Analisis Trade-off

- **Klasik:** Cepat, murah, interpretable, tetapi perlu training dan retraining, kurang adaptif terhadap nuansa bahasa.
- **LLM:** Tanpa training, sangat adaptif, tetapi berbiaya, latensi lebih tinggi, dan ketergantungan pada pihak ketiga.

Cara Menjalankan

1. Clone repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Set environment variable: `export GEMINI_API_KEY="your_api_key"`
4. Jalankan notebook: `jupyter notebook notebook/experiment_notebook.ipynb`
