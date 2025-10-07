# Anomaly Detection pada Access Log Web Server menggunakan Isolation Forest

## Latar Belakang
Dalam sistem web server, setiap aktivitas pengguna akan tercatat dalam *acces log* yang isinya seperti alamat IP, waktu akses, protokol yang digunakan, hingga jenis perangkat. Namun, tidak semua aktivitas tersebut bersifat normal.

Terkadang muncul aktivitas mencurigakan (*anomali*) seperti:
- Percobaan login berulang dari alamat IP berbeda (*brute force attack*),
- Akses di luar jam kerja,
- Permintaan dari subnet atau lokasi asing.

Deteksi anomali secara manual tidak efisien untuk volume log besar, sehingga diperlukan pendekatan **machine learning berbasis unsupervised**.  
Salah satu metode yang terbukti efektif adalah **Isolation Forest**, yang mampu mengidentifikasi *outlier* dengan kompleksitas rendah dan performa tinggi.

Beberapa penelitian sebelumnya menunjukkan efektivitas metode ini:
1. **Liu, F. T., Ting, K. M., & Zhou, Z.-H. (2008).** *Isolation Forest*. *IEEE International Conference on Data Mining (ICDM)*, 413–422.  
   DOI: [10.1109/ICDM.2008.17](https://doi.org/10.1109/ICDM.2008.17)

2. **Elsaid, S. A. & Binbusayyis, A. (2024).** *An optimized isolation forest based intrusion detection system for heterogeneous and streaming data in the IIoT networks.* *Discover Applied Sciences*, 6, 483.  
   DOI: [10.1007/s42452-024-06165-w](https://doi.org/10.1007/s42452-024-06165-w)

3. **Alqahtani, H. (2022).** *Effectively predicting cyber-attacks through isolation forest learning-based outlier detection.* *Security and Privacy*, 5(1), e212.  
   DOI: [10.1002/spy2.212](https://doi.org/10.1002/spy2.212)

4. **Tran, Q. N., & Nguyen, H. T. (2024).** *Web Traffic Anomaly Detection Using Isolation Forest.* *Informatics*, 11(4), 83.  
   DOI: [10.3390/informatics11040083](https://doi.org/10.3390/informatics11040083)

Temuan-temuan tersebut memperkuat dasar ilmiah bahwa **Isolation Forest** efektif digunakan untuk mendeteksi perilaku abnormal dalam log web server dengan efisiensi tinggi.

---

## Tujuan
Penelitian ini bertujuan untuk:
1. Mengidentifikasi aktivitas tidak normal pada access log web server.  
2. Mengimplementasikan algoritma **Isolation Forest** sebagai metode *unsupervised anomaly detection*.  
3. Menghasilkan *anomaly score* yang dapat membantu administrator dalam menemukan pola aktivitas mencurigakan.

---

## Mengapa Isolation Forest?

Berdasarkan artikel:
> [Mendeteksi Anomali dengan Isolation Forest – Cara Mudah Menemukan Outlier dalam Data](https://medium.com/@krisawahyukurniawan_82470/mendeteksi-anomali-dengan-isolation-forest-cara-mudah-menemukan-outlier-dalam-data-872a96b4141d)

Isolation Forest bekerja dengan prinsip bahwa **anomali lebih mudah diisolasi dibandingkan data normal**.  
Setiap pohon (*tree*) dalam model melakukan pemisahan acak (random split), dan data yang cepat terpisah dari yang lain dianggap sebagai **outlier**.

---

## Penjelasan Matematis Isolation Forest

Secara matematis, *anomaly score* dalam Isolation Forest dirumuskan sebagai:

![alt text](image.png)

- h(x) adalah path length, yaitu panjang jalur yang dibutuhkan untuk mengisolasi titik data x dalam pohon keputusan. Semakin cepat suatu titik data terisolasi, semakin pendek jalurnya.
- E(h(x)) adalah rata-rata panjang jalur (path length) dari semua pohon keputusan yang digunakan dalam model. Rata-rata ini menggambarkan seberapa cepat titik data pada umumnya dapat diisolasi.
- c(n) adalah faktor penyesuaian yang bergantung pada jumlah sampel n dalam dataset, yang memastikan perhitungan path length yang tepat sesuai dengan ukuran dataset.
---