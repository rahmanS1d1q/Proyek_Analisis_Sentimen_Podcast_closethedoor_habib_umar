# 🎙️ Proyek Analisis Sentimen Podcast *Close The Door* (Habib Umar)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.5-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 🧠 Deskripsi Proyek

Proyek ini merupakan implementasi **Analisis Sentimen** terhadap komentar-komentar pada video YouTube podcast *Close The Door* yang menampilkan **Habib Umar**.  
Tujuan utamanya adalah untuk memahami **reaksi publik terhadap konten religius** dengan mengklasifikasikan komentar menjadi tiga kategori sentimen:
- 😃 **Positif**
- 😐 **Netral**
- 😠 **Negatif**

Pendekatan ini menggunakan teknik **Natural Language Processing (NLP)** dengan berbagai algoritma Machine Learning untuk membandingkan efektivitas antar model.

---

## 🌟 Fitur Utama

- 🔍 **Scraping otomatis** komentar dari YouTube menggunakan Python.  
- 🧹 **Preprocessing teks**: pembersihan tanda baca, lowercasing, dan penghapusan stopword.  
- 🏷️ **Weak Labeling**: pelabelan semi-otomatis berdasarkan kata kunci sentimen.  
- ⚙️ **Tiga eksperimen pelatihan model**: SVM, Random Forest, dan Logistic Regression.  
- 📊 **Evaluasi performa model** dengan metrik akurasi, F1-score, dan confusion matrix.  
- 💬 **Inference real-time** untuk memprediksi sentimen komentar baru.

---

## ⚙️ Skema Eksperimen Pelatihan Model

| **Eksperimen** | **Algoritma** | **Ekstraksi Fitur** | **Rasio Data (Train/Test)** | **Tujuan** |
|----------------|----------------|----------------------|------------------------------|-------------|
| **A** | SVM (Support Vector Machine) | TF-IDF | 80/20 | Membangun baseline klasik untuk membandingkan performa model lain dan menguji efektivitas representasi berbasis frekuensi kata. |
| **B** | Random Forest | Word2Vec | 70/30 | Mengevaluasi kemampuan model ensemble dalam memanfaatkan representasi semantik (Word2Vec) untuk memahami konteks makna antar kata. |
| **C** | Logistic Regression | TF-IDF | 80/20 | Menguji pendekatan linear sederhana yang efisien secara komputasi namun tetap kompetitif dalam akurasi. |

---

## 📊 Hasil dan Evaluasi

| **Eksperimen** | **Algoritma** | **Ekstraksi Fitur** | **Akurasi Test** | **Keterangan** |
|----------------|----------------|----------------------|------------------|----------------|
| **A** | SVM | TF-IDF | **92%** | Model terbaik, stabil dan konsisten pada data validasi. |
| **B** | Random Forest | Word2Vec | **81%** | Model tradisional berbasis embedding, cukup baik namun sensitif pada variasi data. |
| **C** | Logistic Regression | TF-IDF | **91%** | Model ringan dan cepat dengan performa kompetitif. |

📈 **Kesimpulan:**  
Model **SVM + TF-IDF** menghasilkan performa terbaik (**92%**) dan menjadi model utama dalam analisis ini,  
disusul oleh **Logistic Regression (91%)** dan **Random Forest (81%)**.

---

## 📑 Insight dari Analisis

Dari hasil analisis terhadap lebih dari **30.000 komentar YouTube**, diperoleh distribusi sentimen sebagai berikut:

| Sentimen | Jumlah Komentar | Persentase |
|-----------|-----------------|-------------|
| Positif 😊 | 18.200 | 60.6% |
| Netral 😐 | 7.500 | 25.0% |
| Negatif 😠 | 4.300 | 14.4% |

Mayoritas komentar bernada **positif**, mencerminkan antusiasme dan apresiasi tinggi dari penonton terhadap kehadiran **Habib Umar** di podcast *Close The Door*.

---

## 🧩 Struktur Proyek

