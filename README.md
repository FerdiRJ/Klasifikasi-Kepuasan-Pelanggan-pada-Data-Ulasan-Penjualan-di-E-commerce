# Klasifikasi-Kepuasan-Pelanggan-pada-Data-Ulasan-Penjualan-di-E-commerce
Proyek ini merupakan tugas akhir untuk mata kuliah Pemrosesan Teks pada semester 3 yang bertujuan untuk menganalisis kepuasan pelanggan berdasarkan ulasan produk di platform e-commerce Tokopedia. Dalam proyek ini, kami melakukan proses pengumpulan, pembersihan, dan pemrosesan data ulasan untuk membangun model machine learning yang dapat mengklasifikasikan tingkat kepuasan pelanggan menjadi tiga kategori: puas, netral, dan tidak puas. Kami menggunakan berbagai teknik pemrosesan teks dan algoritma klasifikasi untuk mengevaluasi model dan memberikan wawasan tentang faktor-faktor yang mempengaruhi kepuasan pelanggan.

## 🔍 Tujuan Proyek

1. **Menganalisis Data Ulasan:** Mengumpulkan dan menganalisis ulasan produk dari platform e-commerce Tokopedia untuk mengevaluasi kepuasan pelanggan.
2. **Membangun Model Klasifikasi:** Membangun model machine learning menggunakan teknik pemrosesan teks dan algoritma klasifikasi untuk mengkategorikan ulasan menjadi tiga label kepuasan: puas, netral, dan tidak puas.
3. **Evaluasi Model:** Mengevaluasi kinerja model dengan berbagai metode ekstraksi fitur dan algoritma klasifikasi untuk menentukan pendekatan terbaik dalam memprediksi kepuasan pelanggan.
4. **Pemberian Rekomendasi:** Menyediakan rekomendasi untuk pelaku bisnis berdasarkan hasil analisis untuk meningkatkan kualitas produk dan layanan.

## 📊 Dataset

Dataset yang digunakan dalam proyek ini diperoleh dari Kaggle dan berisi informasi ulasan produk di Tokopedia dengan 40.607 baris data dan 9 kolom: `Unnamed: 0`, `text`, `rating`, `category`, `product_name`, `product_id`, `sold`, `shop_id`, dan `product_url`. Data ini mencakup ulasan produk, rating, kategori produk, dan informasi terkait yang digunakan untuk analisis.

- **Dataset**: [Tokopedia Product Reviews](https://www.kaggle.com/datasets/farhan999/tokopedia-product-reviews)

## 🛠️ Metode

1. **Pengumpulan Data:** Mengambil data ulasan dari Kaggle.
2. **Pembersihan Data:** Menghapus kolom yang tidak diperlukan dan membagi data menjadi tiga kategori utama: pertukangan, elektronik, dan fashion.
3. **Pre-processing:** Melakukan tahap pre-processing seperti lowercase, penghapusan tautan, angka, tanda baca, dan tokenisasi untuk membersihkan data.
4. **Labeling:** Mengkategorikan ulasan ke dalam label kepuasan: 2 untuk puas, 1 untuk netral, dan 0 untuk tidak puas.
5. **Pembagian Data:** Membagi data menjadi set data train (70%) dan data test (30%).
6. **Ekstraksi Fitur:** Mengubah data teks menjadi representasi numerik menggunakan metode seperti BOW, N-Gram, dan TF-IDF.
7. **Resampling:** Mengatasi ketidakseimbangan kelas dengan downsampling untuk kelas mayor dan oversampling untuk kelas minor.
8. **Klasifikasi:** Menerapkan berbagai algoritma seperti Random Forest, SVM, Decision Tree, Naive Bayes, dan KNN untuk mengklasifikasikan ulasan.
9. **Evaluasi Model:** Mengukur kinerja model menggunakan metrik evaluasi seperti akurasi, presisi, recall, dan F1-score.
10. **Iterasi dan Peningkatan:** Mengoptimalkan model melalui penyesuaian parameter dan pemilihan metode ekstraksi fitur.

## 📈 Hasil dan Pembahasan

Hasil evaluasi menunjukkan bahwa model tanpa resampling umumnya memiliki akurasi lebih baik dibandingkan dengan model yang menggunakan resampling. Model Random Forest dan SVM dengan ekstraksi fitur TF-IDF menunjukkan hasil yang baik dalam mengklasifikasikan kepuasan pelanggan di seluruh kategori produk.

| Kategori   | Model Tanpa Resampling | Model Dengan Resampling |
|------------|-------------------------|-------------------------|
| **Fashion** | 93%                     | 71%-89%                 |
| **Elektronik** | 93%                 | 65%-86%                 |
| **Pertukangan** | 94%-95%              | 47%-93%                 |
