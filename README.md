#  Deteksi Komentar Spam YouTube dengan Klasifikasi Manual

## 📄 Deskripsi Proyek
Proyek ini membangun sistem klasifikasi untuk mendeteksi komentar spam di YouTube **tanpa menggunakan library machine learning seperti scikit-learn atau TensorFlow**. Semua tahapan mulai dari preprocessing, ekstraksi fitur, pembangunan model, hingga evaluasi dilakukan secara manual menggunakan Python murni.

## 🎯 Tujuan
- Mendeteksi komentar spam secara otomatis dari data teks komentar YouTube.
- Membandingkan performa empat algoritma klasifikasi teks.
- Melakukan **hyperparameter tuning manual** untuk mengoptimalkan hasil klasifikasi.
- Memberikan pemahaman mendalam tentang pembuatan model machine learning dari nol.

## 📦 Dataset
- Berasal dari komentar YouTube yang dilabeli secara biner:  
  `1 = spam`, `0 = ham`.
- Fitur yang digunakan:  
  - `CONTENT` → sebagai input teks.  
  - `CLASS` → sebagai label target.

## 🧹 Preprocessing Data
- **Lowercasing**
- **Pembersihan karakter non-alfabetik**
- **Tokenisasi manual**
- Disimpan dalam bentuk token untuk proses selanjutnya.

## 🔍 Ekstraksi Fitur
- Metode: **Manual Bag-of-Words (BoW)**
- Dua representasi vektor:
  - Frekuensi kata
  - Kehadiran biner

## 🤖 Model yang Dibangun
Seluruh model dibangun manual, tidak menggunakan model dari library.

### 1. Multinomial Naive Bayes *(Baseline)*
- Menggunakan frekuensi kata.
- Sensitif terhadap spam (recall tinggi).

### 2. Bernoulli Naive Bayes
- Menggunakan representasi biner.
- Sangat selektif (presisi tinggi).

### 3. Logistic Regression
- Dibangun dari nol dengan **gradient descent**.
- Hyperparameter: learning rate, epochs.

### 4. Perceptron
- Model sederhana dari neural network.
- Performa terbaik dari semua model.

## 📊 Evaluasi & Hasil
- Metrik evaluasi:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
- Dataset testing digunakan untuk evaluasi semua model.
- **Hasil terbaik** diperoleh oleh **Perceptron**:
  - Akurasi: 0.9079
  - F1-Score: 0.9022

---
