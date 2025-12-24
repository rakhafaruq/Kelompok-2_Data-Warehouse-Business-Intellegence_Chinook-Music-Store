# 🎵 Proyek Data Warehouse & Business Intelligence: Chinook Music Store

## 📌 Ringkasan Proyek
Proyek ini merupakan implementasi solusi **Business Intelligence (BI)** lengkap untuk Chinook Music Store, dengan fokus utama pada **Perspektif Finansial**. Tujuan dari proyek ini adalah menganalisis tren pendapatan, melakukan segmentasi pelanggan, dan memprediksi penjualan di masa depan untuk mendukung pengambilan keputusan strategis tingkat eksekutif.

**Tujuan Utama:**
1.  Merancang **Data Warehouse** menggunakan skema bintang (*Star Schema*).
2.  Melakukan proses **ETL** (*Extract, Transform, Load*) untuk integrasi data.
3.  Mengimplementasikan **Data Mining** (Clustering & Regresi) untuk analisis prediktif.
4.  Mengembangkan **Dashboard Interaktif** untuk pemantauan KPI.

## 📊 1. Desain Data Warehouse
Kami mentransformasi database transaksional (3NF) menjadi **Star Schema** yang dioptimalkan untuk query analitik (OLAP).

- **Tabel Fakta:** `Fact_Sales` (Measure: Quantity, Amount).
- **Tabel Dimensi:**
  - `Dim_Pelanggan` (Lokasi, Email).
  - `Dim_Waktu` (Tahun, Kuartal, Bulan, Hari).
  - `Dim_Musik` (Track, Genre, Album, Artis).

---

## 🧠 2. Implementasi Data Mining

### A. Segmentasi Pelanggan (Clustering)
**Algoritma:** K-Means Clustering
**Tujuan:** Mengelompokkan pelanggan berdasarkan perilaku belanja RFM (*Recency, Frequency, Monetary*) untuk mengidentifikasi pelanggan bernilai tinggi.

| Cluster | Label | Insight & Rekomendasi |
| :--- | :--- | :--- |
| **0** | Standar | Pelanggan reguler dengan pengeluaran rata-rata. Pertahankan layanan standar. |
| **1** | Dormant | Pelanggan tidak aktif (>1.5 tahun), risiko *churn* tinggi. Perlu strategi *win-back*. |
| **2** | **Premium** | **ARPC Tertinggi ($44.8)**, sangat aktif. Prioritas utama untuk program loyalitas. |

### B. Peramalan Penjualan (Regression)
**Algoritma:** Linear Regression
**Tujuan:** Memprediksi Total Pendapatan Bulanan untuk 6 bulan ke depan.
**Hasil Analisis:**
- **Slope (Kemiringan):** `-0.01` (Menunjukkan Tren Stagnan/Sedikit Menurun).
- **Kesimpulan:** Bisnis berada dalam fase jenuh. Diperlukan intervensi pemasaran segera atau ekspansi katalog produk baru.

---

## 📈 3. Visualisasi Dashboard
Executive Dashboard dirancang untuk memvisualisasikan indikator kinerja utama (KPI) berikut:
- **Total Revenue:** Posisi keuangan perusahaan secara real-time.
- **ARPC (Rata-rata Pendapatan per Pelanggan):** Tolok ukur nilai ekonomi pelanggan.
- **Tren Penjualan:** Perbandingan data historis vs data prediksi (Forecasting).

🔗 **[Lihat Dashboard Langsung (Klik Disini)](https://lookerstudio.google.com/reporting/4123ca0f-b964-4568-9593-9d7634a63a9d)**

---
