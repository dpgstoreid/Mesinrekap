# 📄 Mesinrekap — Sistem Cetak Laporan Perjalanan Dinas & Cash Advance

Aplikasi web ringan berbasis *Single-File HTML* untuk membuat, merekonsiliasi, dan mencetak **Formulir Pertanggungjawaban Cash Advance (Uang Muka Dinas)** secara cepat, rapi, dan presisi dalam **1 halaman A4**. Dirancang khusus untuk kebutuhan operasional dan keuangan **PT DPG STOREID**.

🔗 **Live Demo / Akses Aplikasi:** [https://dpgstoreid.github.io/Mesinrekap/](https://dpgstoreid.github.io/Mesinrekap/)

---

## ✨ Fitur Utama

* **🖨️ Presisi Cetak 1 Halaman A4 (`@media print`):** Tata letak otomatis menyesuaikan ukuran kertas A4 *portrait* tanpa terpotong atau meluber ke halaman kedua.
* **🔄 3 Mode Tampilan Realisasi:**
  * **📅 Mode Harian:** Mengelompokkan pengeluaran berdasarkan tanggal transaksi beserta status nota (`[✓ Nota]` / `[Non-Nota]`).
  * **📑 Mode Kategori Pos:** Mengelompokkan pengeluaran berdasarkan pos biaya (Uang Makan, Hotel, BBM, Tol/Parkir, Operasional Kios, Lain-lain).
  * **📊 Mode 2-Kolom Rinci:** Menampilkan tabel transaksi baris demi baris secara padat dan kronologis.
* **🧮 Rekonsiliasi Kas Otomatis:** Menghitung otomatis selisih antara *Total Kas Diterima (A)* dan *Total Pengeluaran Riil (B)* dengan indikator status **Lebih Bayar (Kembali ke Kasir)**, **Kurang Bayar (Klaim Reimburse)**, atau **Saldo Nihil (Pas)**.
* **📊 Ekspor ke Microsoft Excel (`.xlsx`):** Unduh data uang masuk dan realisasi pengeluaran langsung menjadi file Excel 2 *sheet* menggunakan integrasi SheetJS.
* **💬 Generator Ringkasan WhatsApp:** Salin laporan ringkas berformat teks tebal/miring siap kirim ke grup atau atasan via WhatsApp hanya dengan 1 klik.
* **🔗 Berbagi Data via URL & Backup JSON:**
  * Simpan data ke file `.json` untuk arsip lokal dan muat kembali kapan saja.
  * Bagikan seluruh isi form melalui *Shareable Link* (URL Hash Base64) tanpa memerlukan database server.
* **💾 Auto-Save (`localStorage`):** Data tersimpan otomatis di peramban sehingga tidak hilang saat halaman tidak sengaja dimuat ulang.

---

## 🛠️ Teknologi yang Digunakan

* **HTML5 & Vanilla JavaScript** (Tanpa *framework* berat, langsung jalan di *browser*)
* **Tailwind CSS** (via CDN) untuk antarmuka pengguna dan tata letak cetak
* **Lucide Icons** untuk ikonografi antarmuka
* **SheetJS (xlsx)** untuk pembuatan file spreadsheet `.xlsx` di sisi klien

---

## 🚀 Cara Penggunaan

1. Buka link aplikasi di **[dpgstoreid.github.io/Mesinrekap](https://dpgstoreid.github.io/Mesinrekap/)** atau buka file `index.html` langsung di browser.
2. **Isi Data Kunjungan:** Masukkan nama perusahaan, pelaksana, departemen, kota tujuan, nomor referensi CA, dan tanggal dinas di panel sebelah kiri.
3. **Input Kas & Pengeluaran:** Tambahkan daftar penerimaan Cash Advance dan rincian pengeluaran lapangan (lengkap dengan centang ketersediaan nota fisik).
4. **Pilih Mode & Cetak:** Pilih tampilan tabel (**Harian**, **Kategori**, atau **2-Kolom**), lalu klik tombol **Cetak A4 (1 Lembar)** atau tekan `Ctrl + P`.
