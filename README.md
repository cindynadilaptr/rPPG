# Real-time rPPG (Remote Photoplethysmography) Implementation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Face%20Detection-orange)

**Nama:** Cindy Nadila Putri  
**NIM:** 122140002 
**Mata Kuliah:** Sistem Teknologi Multimedia

---

## Deskripsi Tugas
Proyek ini bertujuan untuk mengimplementasikan sistem **Remote Photoplethysmography (rPPG)** sederhana menggunakan webcam. Sistem ini mampu mendeteksi detak jantung (Heart Rate/BPM) seseorang secara *contactless* (tanpa kontak fisik) dengan menganalisis perubahan warna kulit wajah akibat aliran darah.

Kode dikembangkan dalam format **Jupyter Notebook (`.ipynb`)** untuk memudahkan demonstrasi per blok pemrosesan sinyal.

### Fitur Utama
Sesuai dengan spesifikasi tugas, sistem ini mencakup:
1.  **Face Detection & ROI:** Menggunakan **MediaPipe** untuk mendeteksi wajah dan menentukan Region of Interest (ROI) pada area dahi secara otomatis.
2.  **Signal Extraction:** Mengekstraksi rata-rata kanal **Hijau (Green Channel)** yang sensitif terhadap penyerapan hemoglobin.
3.  **Signal Processing:**
    * **Detrending:** Menghilangkan *drift* pencahayaan.
    * **Bandpass Filter:** Filter Butterworth (0.9 - 3.0 Hz) untuk mengambil rentang detak jantung manusia (54 - 180 BPM).
4.  **BPM Estimation:** Menghitung denyut nadi secara *real-time* menggunakan algoritma *Peak Detection*.
5.  **Visualization:** Menampilkan grafik sinyal detak jantung dan nilai BPM secara *real-time* (Overlay pada video).

---

## Prasyarat & Instalasi

Pastikan Anda telah menginstal Python. Library yang digunakan tercantum dalam `requirements.txt`.

### 1. Clone Repository
```bash
git clone https://github.com/cindynadilaptr/rPPG.git
cd [Nama Folder Repo] 
```

### 2. Install Dependencies
Disarankan untuk menggunakan virtual environtment

```bash
pip install -r requirements.txt
```

### 3. Jalankan Kode Program
Buka terminal/command prompt di dalam folder proyek. Jalankan Jupyter Notebook:

```bash
jupyter notebook rPPG.ipynb
```

