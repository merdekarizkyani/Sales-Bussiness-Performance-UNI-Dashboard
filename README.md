# Sales-Bussiness-Performance-UNI-Dashboard
Dashboard interaktif ini dirancang untuk memantau, menganalisis, dan memvisualisasikan performa penjualan serta tren bisnis secara menyeluruh selama periode Januari – Desember 2025. Dashboard ini menyajikan indikator kinerja utama (KPI) finansial, analisis wilayah, performa produk, hingga kontribusi saluran penjualan (sales channels).

<img width="1322" height="740" alt="Dashboard uni" src="https://github.com/user-attachments/assets/ff75c832-a954-46cc-9d7c-77598bf72ae2" />

## Tools 
1. Power BI Desktop: Untuk manipulasi data (Power Query), pemodelan data (DAX), serta desain visualisasi dashboard interaktif.
2. GitHub: Untuk repositori kode, dokumentasi proyek (README.md), dan portofolio data analisis.

## 1. Business Insights
a. Penjualan 2025: Penjualan tertinggi diraih pada Juni 2025 (~Rp2,96M) dan Oktober 2025 (~Rp2,95M), sedangkan penjualan terendah terjadi pada Maret 2025 (~Rp2,33M).
b. Pertumbuhan YoY (2024 vs 2025): Peningkatan/lonjakan penjualan tertinggi dibanding tahun lalu terjadi pada Maret (dari Rp890Jt pada 2024 naik pesat ke Rp2,33M pada 2025), sedangkan pertumbuhan terendah/terkecil terjadi pada Oktober (karena basis penjualan Oktober 2024 sudah sangat tinggi di kisaran Rp1,62M).
c. Kategori Utama: Personal Care menjadi kategori penyumbang omzet terbesar yaitu 32,38% (sekitar Rp8,72M) dari total pendapatan.
d. Top Product: Lifebuoy menjadi produk terlaris (top-selling product) dengan total penjualan mencapai Rp3.416.025.000.
e. Kontribusi Wilayah: Wilayah Jawa menjadi penyumbang pendapatan terbesar secara geografis dengan porsi 46,64% (hampir separuh dari total revenue).
f. Saluran Penjualan: Modern Trade menjadi saluran distribusi dengan volume penjualan unit tertinggi yaitu sebesar 176.110 unit (diikuti Traditional Trade 143.052 unit).

## 2. Pertanyaan Bisnis 
1. Mengapa terjadi penurunan volume penjualan pada bulan Maret 2025 jika dibandingkan dengan bulan-bulan lainnya di tahun 2025?
2. Bagaimana strategi mendorong penetrasi pasar di luar wilayah Jawa (seperti Bali, Nusa Tenggara, Maluku, dan Papua) yang saat ini masih di bawah 6%?
3. Apa strategi optimasi margin untuk saluran E-commerce dan Direct Sales agar mampu menyamai performa Modern Trade?

## 3. Peluang & Rekomendasi Strategis
1. Tingkatkan Stok & Promosi Personal Care: Alokasikan inventaris lebih besar pada produk FMCG seperti Lifebuoy dan Pepsodent menjelang kuartal akhir (Q3-Q4) untuk memaksimalkan tren penjualan tinggi.
2. Tingkatkan Penetrasi Pasar Luar Jawa: Lakukan program kampanye pemasaran lokal dan evaluasi rantai pasok (supply chain) di wilayah Sumatera, Kalimantan, dan Timur Indonesia untuk memperluas pangsa pasar.
3. Tingkatkan Performa Saluran Digital (E-commerce): Berikan penawaran eksklusif atau paket bundling di E-commerce untuk menggenjot kuantitas unit yang masih tertinggal dibanding Modern/Traditional Trade.

## 4. Ringkasan Visualisasi Dashboard
1. KPI Cards: Menampilkan 4 metrik utama (Total Revenue, Total Unit, Total Customers, AOV).
2. Sales Trend (Combo Chart): Grafik batang & garis untuk membandingkan tren bulanan Sales 2025 vs 2024.
3. Sales by Category (Donut Chart): Proporsi porsi omzet per kategori (Personal Care, Home Care, dll).
4. Top 5 Products & Regional Sales (Bar Charts): Peringkat 5 produk teratas dan kontribusi persentase per wilayah.
5. Sales by Channel (Column Chart): Kuantitas penjualan unit berdasarkan kanal distribusi.

## 5. Pemprosesan Data & DAX Measures
A. Pembersihan Data (Data Cleaning)
- Validasi Data: Menghapus entitas ganda (duplicate rows) dan menangani nilai kosong (null/missing values).
- Format Tipe Data: Memastikan Order Date bersumber Date, Sales Revenue & Price ke Currency, serta Quantity ke Whole Number.
- Transformasi Data: Standardisasi penulisan nama produk/kategori serta pengelompokan Region Indonesia.

B. Summary DAX Measures Utama
| No |Measure |
| :--- | :--- |
| **1.** | Total Sales = SUM(Sales[Sales Amount])  |
| **2.** | Total Unit = SUM(Sales[Quantity]) |
| **3.** | Total Customers = DISTINCTCOUNT(Sales[Customer ID]) |
| **4.** | Avg Order Value = DIVIDE([Total Sales], COUNT(Sales[Order ID]), 0) |
