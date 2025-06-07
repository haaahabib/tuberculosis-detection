# Deteksi Tuberkulosis (TB) Menggunakan Citra X-ray dengan ResNet18

Ini adalah repositori kode untuk proyek penelitian yang berfokus pada deteksi Tuberkulosis (TB) dari citra X-ray menggunakan model deep learning ResNet18. Penelitian ini bertujuan untuk mengembangkan sistem klasifikasi yang akurat, konsisten, dan dapat diinterpretasi Grad-CAM untuk mendukung diagnosis tuberkulosis (TB).

## Daftar Isi

1.  [Tentang Proyek](#1-tentang-proyek)
2.  [Fitur Utama](#2-fitur-utama)
3.  [Hasil Penelitian](#3-hasil-penelitian)
4.  [Struktur Repositori](#4-struktur-repositori)
5.  [Dataset](#5-dataset)
6.  [Cara Menggunakan](#6-cara-menggunakan)
7.  [Lisensi](#7-lisensi)

---

## 1. Tentang Proyek

Proyek ini mengimplementasikan model Convolutional Neural Network (CNN) *ResNet18* untuk mengklasifikasikan citra X-ray dada menjadi "Normal" atau "Tuberkulosis". Penelitian ini menggunakan dataset yang seimbang _(balanced)_, menerapkan *K-Fold Cross Validation*, serta memanfaatkan *Grad-CAM* untuk meningkatkan reliabilitas dan transparansi model terhadap keputusan model.

## 2. Fitur Utama

* **Deteksi Tuberkulosis:** Menggunakan *ResNet18* untuk klasifikasi citra X-ray dengan hasil yang konsisten.
* **Penggunaan Dataset Seimbang:** Menggunakan 3.500 citra X-ray normal dan 3.500 citra X-ray TB untuk mengurangi *bias kelas*, menghasilkan model yang lebih representatif.
* **Evaluasi Model:** Penerapan *K-Fold Cross Validation* (5-fold) untuk memastikan konsistensi dan generalisasi model.
* **Interpretasi Visual:** Integrasi *Grad-CAM* untuk memvisualisasikan area penting pada citra yang menjadi dasar prediksi model, meningkatkan transparansi dan pemahaman model.

## 3. Hasil Penelitian

Berdasarkan implementasi dan evaluasi menggunakan *K-Fold Cross Validation* (5-fold), model ResNet18 yang dikembangkan menunjukkan performa yang sangat baik:

* **Akurasi Keseluruhan:** **99.57%** (0.9957)
* **Pengurangan Bias Kelas**: Penggunaan dataset yang seimbang secara efektif mengurangi bias terhadap kelas mayoritas, menghasilkan model yang lebih *robust*.
* **Interpretasi yang Jelas:** *Grad-CAM* berhasil menyoroti area relevan pada citra X-ray, meningkatkan pemahaman tentang keputusan model oleh tenaga ahli.

## 4. Struktur Repositori

* `tuberculosis_detection.ipynb`: *Notebook* Google Colab utama yang berisi seluruh *code* implementasi, pelatihan, dan evaluasi *model*. Ini adalah *file* yang bisa langsung dibuka di Google Colab.
* `tuberculosis_detection.py`: Versi *script* Python dari *code* yang sama, cocok untuk dijalankan di lingkungan lokal atau server.
* `README.md`: *File* ini sendiri, yang memberikan gambaran umum tentang proyek.

## 5. Dataset

*Dataset* yang digunakan dalam penelitian ini adalah **"Tuberculosis (TB) Chest X-ray Dataset"** yang tersedia secara publik di Kaggle.
* **Jumlah Citra:** Terdiri dari total 7.000 citra *X-ray*, dibagi menjadi:
    * 3.500 citra *X-ray* Normal
    * 3.500 citra *X-ray* Tuberkulosis
* **Sumber:** [Kaggle: Tuberculosis (TB) Chest X-ray Dataset](https://www.kaggle.com/datasets/scipygaurav/tuberculosis-tb-chest-x-ray-cleaned-database)

## 6. Cara Menggunakan

1.  **Akses *Notebook* Google Colab:**
    * Buka `tuberculosis_detection.ipynb` langsung di Google Colab.
    * Anda dapat menjalankan setiap sel untuk melihat alur kerja mulai dari persiapan data, pelatihan model, hingga evaluasi dan interpretasi.

2.  **Menjalankan di Lingkungan Lokal (Opsional):**
    * Kloning repositori ini
    * Jalankan *script* `tuberculosis_detection.py`.
    
---
