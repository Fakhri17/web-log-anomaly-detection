## Alur Penelitian



┌─────────────────────────────────┐
│ **1. Pengumpulan Data**         │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **2. Preprocessing Data**       │
│    - Parsing Log                │
│    - Cleaning Data              │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **3. Feature Engineering**      │
│    - Ekstraksi Fitur            │
│    - Feature Selection          │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **4. Pelabelan Data**           │
│    - Anomaly Detection          │
│    - Manual Labeling            │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **5. Normalisasi Data**         │
│    - StandardScaler             │
│    - One-Hot Encoding           │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **6. Pemodelan**                │
│    - Isolation Forest           │
│    - Training Model             │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **7. Evaluasi Model**           │
│    - Accuracy, Precision        │
│    - Recall, F1-Score           │
│    - Confusion Matrix           │
└────────────┬────────────────────┘
             │
┌────────────▼────────────────────┐
│ **8. Analisis Hasil**           │
└─────────────────────────────────┘


# Kesesuaian Alur Penelitian dengan Judul Skripsi

Alur penelitian yang kamu susun **sudah sangat cocok** untuk skripsi dengan judul:

**“Deteksi Anomali pada Access Log Web Server Nginx Menggunakan Algoritma Isolation Forest”**

Berikut alasan detailnya:

---

## ✅ 1. Pengumpulan Data
Tahap ini benar karena kamu bekerja dengan **access log Nginx** yang menjadi sumber dataset utama.

---

## ✅ 2. Preprocessing Data
Access log memiliki format tidak terstruktur sehingga perlu:
- Parsing log
- Cleaning data
- Menghapus noise

Tahapan ini **wajib** sebelum masuk ke tahap pemodelan.

---

## ✅ 3. Feature Engineering
Sangat relevan untuk mengubah log menjadi fitur numerik, seperti:
- IP frequency
- Status code distribution
- Request count
- URL/path length

Tahap ini *harus ada* pada penelitian anomaly detection berbasis log.

---

## ✅ 4. Pelabelan Data
Cocok karena:
- Isolation Forest adalah unsupervised, tapi **evaluasi butuh label**.
- Bisa menggunakan manual labeling atau heuristik.

---

## ✅ 5. Normalisasi Data
Tahap normalisasi data penting untuk:
- Menyelaraskan skala fitur agar model bekerja optimal
- Menggunakan teknik seperti StandardScaler dan One-Hot Encoding
- Mengurangi bias akibat perbedaan satuan/skala pada data

Normalisasi memastikan semua fitur dapat berkontribusi secara proporsional dalam proses pemodelan.

---

## ✅ 6. Pemodelan
Tahap inti skripsi kamu:
- Penerapan algoritma **Isolation Forest**
- Training model

Sudah sesuai dengan judul.

---

## ✅ 7. Evaluasi Model
Kamu menggunakan metrik yang benar:
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix  

Metrik-metrik ini adalah standar dalam penelitian anomaly detection.

---

## ✅ 8. Analisis Hasil
Bagian ini penting untuk:
- Menjawab rumusan masalah
- Mendukung kesimpulan
- Memberikan insight akademik

---

# ⭐ Kesimpulan
Alur penelitianmu **sangat ideal dan sesuai standar skripsi S1** untuk topik Isolation Forest + Access Log.  
Alur tersebut sudah:
- Logis  
- Akademis  
- Lengkap  
- Sesuai pipeline machine learning  

Jika kamu ingin, saya bisa buatkan:
- **Flowchart Bab III**  
- **Diagram alir resmi**  
- **Versi ringkas untuk metodologi skripsi**
