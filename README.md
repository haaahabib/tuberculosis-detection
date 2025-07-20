# Deteksi Tuberkulosis Menggunakan ResNet-18 dan Grad-CAM

Proyek ini bertujuan untuk mengembangkan sistem deteksi tuberkulosis (TBC) yang sangat akurat dari citra Rontgen (X-ray) paru-paru menggunakan arsitektur *deep learning* **ResNet-18**. Untuk meningkatkan kepercayaan dan interpretasi model, proyek ini juga mengimplementasikan **Grad-CAM** untuk visualisasi area fokus pada gambar.

---

## Daftar Isi

1.  [Latar Belakang](#latar-belakang)
2.  [Tujuan Proyek](#tujuan-proyek)
3.  [Dataset](#dataset)
4.  [Metodologi](#metodologi)
5.  [Hasil Evaluasi Model](#hasil-evaluasi-model)
6.  [Tech Stack](#tech-stack)
7.  [Cara Menjalankan Proyek](#cara-menjalankan-proyek)
8.  [Profil Pembuat](#profil-pembuat)

---

## Latar Belakang

Diagnosis tuberkulosis (TBC) yang cepat dan akurat adalah kunci untuk penanganan yang efektif. Meskipun citra Rontgen adalah alat diagnostik utama, interpretasinya bisa menjadi tantangan. Proyek ini memanfaatkan kekuatan *deep learning*, khususnya model **ResNet-18**, untuk otomatisasi deteksi. Selain itu, untuk mengatasi masalah "kotak hitam" pada model AI, teknik **Grad-CAM (Gradient-weighted Class Activation Mapping)** digunakan untuk memberikan penjelasan visual tentang bagian mana dari citra Rontgen yang menjadi dasar keputusan model.

## Tujuan Proyek

-   Membangun model klasifikasi citra dengan akurasi tinggi menggunakan arsitektur **ResNet-18**.
-   Menerapkan **K-Fold Cross Validation** untuk evaluasi model yang lebih robust dan andal.
-   Menggunakan dataset yang seimbang untuk mengurangi potensi bias pada kelas tertentu.
-   Meningkatkan interpretabilitas model dengan visualisasi **Grad-CAM**, yang menyoroti area patologis yang relevan bagi tenaga medis.

---

## Dataset

Dataset yang digunakan dalam proyek ini terdiri dari kumpulan gambar Rontgen dada (chest X-ray) yang telah dilabeli, yang dibagi menjadi dua kategori: **Normal** dan **Tuberculosis**. Perhatian khusus diberikan untuk menjaga keseimbangan jumlah data antar kelas untuk memastikan model tidak bias.

---

## Metodologi

1.  **Pra-pemrosesan & Augmentasi**: Gambar disiapkan melalui normalisasi dan augmentasi data untuk memperkaya variasi data latih.
2.  **Arsitektur Model**: Menggunakan **ResNet-18**, sebuah arsitektur Convolutional Neural Network (CNN) yang telah terbukti efektif untuk tugas klasifikasi gambar.
3.  **Pelatihan & Validasi**: Model dilatih dan dievaluasi menggunakan metode **K-Fold Cross Validation (dengan 5-fold)**. Pendekatan ini memberikan estimasi performa model yang lebih stabil dan dapat diandalkan dibandingkan pembagian data latih-uji konvensional.
4.  **Interpretasi Model**: Setelah pelatihan, **Grad-CAM** diterapkan pada gambar uji untuk menghasilkan *heatmap* yang menunjukkan area paling berpengaruh dalam pengambilan keputusan model.

---

## Hasil Evaluasi Model

Berdasarkan implementasi dan evaluasi yang ketat, model ResNet-18 yang dikembangkan menunjukkan performa yang luar biasa.

| Metrik | Hasil | Keterangan |
| :--- | :---: | :--- |
| **Akurasi Keseluruhan** | **99.57%** | Performa yang sangat tinggi dan konsisten di seluruh lipatan validasi. |
| **Pengurangan Bias**| Efektif | Penggunaan dataset yang seimbang berhasil mengurangi bias terhadap kelas mayoritas. |
| **Interpretasi Model** | Jelas | Grad-CAM berhasil menyoroti area relevan pada citra X-ray, transparansi model. |

---

## Tumpukan Teknologi

-   **Bahasa Pemrograman**: Python
-   **Framework Deep Learning**: PyTorch / TensorFlow, Keras
-   **Library Utama**:
    -   Pandas & NumPy
    -   Scikit-learn (untuk K-Fold Cross Validation)
    -   Matplotlib & Seaborn
    -   OpenCV

---

## Cara Menjalankan Proyek

1.  **Clone Repositori Ini**
    ```bash
    git clone https://github.com/haaahabib/tuberculosis-detection.git
    ```
2.  **Masuk ke Direktori Proyek**
    ```bash
    cd tuberculosis-detection
    ```
3.  **Install Library yang Dibutuhkan**
    ```bash
    pip install torch torchvision pandas numpy scikit-learn matplotlib seaborn opencv-python jupyter
    ```
4.  **Jalankan Jupyter Notebook**
    Buka dan jalankan file `main.ipynb` untuk melihat keseluruhan alur kerja proyek.
    ```bash
    jupyter notebook main.ipynb
    ```

---

## Profil Pembuat

-   **Nama**: Muhammad Habibulloh
-   **NIM**: 202110370311259
-   **GitHub**: [haaahabib](https://github.com/haaahabib)
