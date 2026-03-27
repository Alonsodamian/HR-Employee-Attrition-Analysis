# HR-Employee-Attrition-Analysis

# HR Employee Attrition Analysis

Proyek analisis dan prediksi attrition karyawan untuk perusahaan **Jaya Jaya Maju** menggunakan machine learning.

---

## 📋 Latar Belakang

Jaya Jaya Maju adalah perusahaan multinasional yang berdiri sejak tahun 2000 dengan lebih dari 1.000 karyawan. Perusahaan menghadapi tantangan attrition rate yang tinggi (>10%), sehingga diperlukan analisis mendalam untuk mengidentifikasi faktor penyebab dan membangun model prediktif guna mencegah karyawan keluar.

---

## 🎯 Tujuan

- Mengidentifikasi faktor-faktor utama yang mempengaruhi attrition karyawan
- Membangun model machine learning untuk memprediksi karyawan yang berisiko keluar
- Memberikan rekomendasi bisnis berbasis data

---

## 📁 Struktur Proyek

```
HR-Employee-Attrition-Analysis/
├── employee_data.csv                                    # Dataset
├── Employee-Attrition-and-Performance-Prediction.ipynb # Notebook analisis utama
└── README.md
```

---

## 🔍 Temuan Utama

| Faktor | Insight |
|---|---|
| **OverTime** | 51% karyawan yang keluar bekerja lembur |
| **Stock Option** | 71% karyawan yang keluar tidak memiliki stock option |
| **Job Level** | 64% karyawan yang keluar berada di Entry Level |
| **Marital Status** | 55% karyawan yang keluar berstatus Single |

---

## 🤖 Model Machine Learning

Tiga model dibangun dan dibandingkan:

| Model | Accuracy | ROC AUC |
|---|---|---|
| Random Forest | ~87% | ~0.78 |
| XGBoost | ~87% | ~0.76 |
| Logistic Regression | ~88% | ~0.78 |

**Catatan:** Untuk kasus attrition, *Recall* pada kelas "Leave" lebih diutamakan daripada Accuracy.

---

## 💡 Rekomendasi Bisnis

1. **Batasi Overtime** — Terapkan monitoring beban kerja dan kompensasi yang lebih baik
2. **Perluas Stock Option** — Khususnya untuk karyawan Entry dan Junior Level
3. **Program Retensi Entry Level** — Jalur karir yang jelas, mentorship, dan fast-track promotion
4. **Engagement Karyawan Single** — Program komunitas dan team building
5. **Implementasi Model Prediksi** — Jalankan model secara kuartalan untuk deteksi dini karyawan berisiko

---

## 🛠️ Teknologi yang Digunakan

- **Python 3.9**
- `pandas`, `numpy` — Data manipulation
- `scikit-learn` — Machine learning & evaluasi
- `imbalanced-learn` — SMOTE untuk class imbalance
- `xgboost` — Gradient boosting
- `matplotlib`, `seaborn` — Visualisasi

---

## ⚠️ Keterbatasan

- 412 nilai `Attrition` (~28%) diisi menggunakan prediksi model (bukan label aktual), yang dapat menimbulkan bias
- Model perlu di-retrain secara berkala dengan data terbaru
- Recall pada kelas "Leave" masih dapat ditingkatkan dengan hyperparameter tuning lebih lanjut

---

## 🚀 Cara Menjalankan

1. Clone repository ini
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn imbalanced-learn xgboost matplotlib seaborn jupyter
   ```
3. Jalankan notebook:
   ```bash
   jupyter notebook Employee-Attrition-and-Performance-Prediction.ipynb
   ```
