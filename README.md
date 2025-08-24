# Segmentasi Tumor Otak menggunakan Swin U-Net

Proyek ini adalah implementasi model *deep learning* untuk melakukan segmentasi semantik pada citra MRI otak guna mengidentifikasi area tumor.

## Deskripsi

Tujuan utama proyek ini adalah untuk membangun, melatih, dan mengevaluasi model segmentasi. Perjalanan proyek ini melibatkan dua arsitektur utama:

1.  **Swin U-Net (Baseline V1.1):** Eksperimen awal dilakukan dengan arsitektur modern Swin U-Net. Model ini berhasil dilatih selama 43 epoch dan mencapai **Dice Coefficient ~57%** pada data validasi. Analisis menunjukkan bahwa performa model ini terbatas oleh *overfitting*.
## Dataset

Dataset yang digunakan adalah "Brain Tumor Segmentation" dari Kaggle.
* **Tautan:** [https://www.kaggle.com/datasets/nikhilroxtomar/brain-tumor-segmentation](https://www.kaggle.com/datasets/nikhilroxtomar/brain-tumor-segmentation)
* Dataset ini berisi 3064 citra MRI beserta masker segmentasi yang sesuai.

## Alur Kerja

Notebook `Image_Classification_dengan_Swin_UNet.ipynb` berisi seluruh alur kerja, yang meliputi:

- **Fase 1 & 2:** Pre-processing data (resizing, normalisasi, splitting).
- **Fase 3:** Pembangunan arsitektur, kompilasi, dan proses training.
- **Fase 4:** Evaluasi model pada *test set* dan visualisasi hasil prediksi.

## Hasil Akhir

Model U-Net final berhasil mencapai **Dice Coefficient sebesar 57%** pada data test yang independen. Visualisasi menunjukkan bahwa model mampu mengidentifikasi lokasi umum tumor dengan cukup baik, meskipun presisi pada bagian tepinya masih perlu ditingkatkan.

## Cara Menjalankan

1.  Pastikan Anda memiliki akun Google dan akses ke Google Colab.
2.  Unduh dataset dari tautan Kaggle di atas dan unggah ke Google Drive Anda.
3.  Buka file `.ipynb` di Google Colab.
4.  Sesuaikan *path* direktori data di dalam notebook agar sesuai dengan lokasi di Google Drive Anda.
5.  Jalankan sel-sel secara berurutan.

## Teknologi yang Digunakan
- TensorFlow & Keras
- Python
- Google Colab (dengan GPU L4)
- NumPy, Matplotlib, OpenCV
