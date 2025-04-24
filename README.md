# 📊 Prediksi Pembelian Komputer dengan Decision Tree

Proyek ini merupakan implementasi sederhana dari algoritma **Decision Tree Classifier** untuk memprediksi apakah seseorang akan membeli komputer berdasarkan data demografis seperti usia, pendapatan, status mahasiswa, dan rating kredit. Dataset yang digunakan bersifat kategorikal dan dianalisis menggunakan Python di Jupyter Notebook.

---

## 🗂️ Struktur Proyek
- .
- ├── dataset.csv           # Dataset utama
- ├── notebook.ipynb        # Notebook utama untuk eksplorasi dan modeling
- └── README.md             # Dokumentasi proyek

---

## 🚀 Langkah-langkah

### 1. 📥 Persiapan Data
- Impor pustaka yang dibutuhkan seperti `pandas`, `numpy`, `matplotlib`, `seaborn`, dan `scikit-learn`.
- Muat dataset dari `dataset.csv`.
- Tampilkan data dan lakukan eksplorasi awal (`head`, cek missing value, distribusi target).

### 2. 📊 Eksplorasi dan Visualisasi
- Tampilkan jumlah masing-masing kelas target (`Buys_Computer`).
- Buat visualisasi distribusi target dan **heatmap korelasi antar fitur** (menggunakan LabelEncoder sementara).

### 3. ⚙️ Pra-pemrosesan
- Lakukan **Label Encoding** pada fitur kategorikal:
  - `Age`
  - `Income`
  - `Student`
  - `Credit_Rating`
- Pisahkan fitur (`X`) dan target (`y`).

### 4. 🧪 Split Data
- Pisahkan data menjadi **training** dan **testing set** menggunakan `train_test_split()` dengan **stratify** agar distribusi target seimbang.

### 5. 🌳 Pelatihan Model
- Buat model `DecisionTreeClassifier` dengan kriteria `'entropy'`.
- Atur parameter seperti `max_depth` dan `min_samples_split`.
- Latih model dengan data training.

### 6. ✅ Evaluasi Model
- Lakukan prediksi pada data uji.
- Evaluasi model menggunakan:
  - **Akurasi**
  - **Precision**
  - **Recall**
  - **F1-Score**
  - **Confusion Matrix**
- Visualisasikan hasil **Decision Tree** dan **Feature Importance**.

### 7. 🤖 Prediksi Baru
- Buat fungsi prediksi berdasarkan input manual:
  - Umur
  - Pendapatan
  - Status mahasiswa
  - Rating kredit
- Uji model pada beberapa **contoh pelanggan baru**
