## Alphabet Sign Language Detection
Ini adalah projek python yang menggunakan MediaPipe + Ekstraksi landmark menjadi fitur dan label + Arsitektur MLP untuk membuat model deteksi bahasa isyarat level alfabet secara realtime. Instruksi bisa diakses di [file ini](/instruksi.md)

---
### 1. Persyaratan Sistem

   ⚠️ Compatibility Notice
   
   Proyek ini dikembangkan dan diuji menggunakan:

   - Python 3.9.x
   - TensorFlow 2.15.0
   - MediaPipe 0.10.14
   - NumPy 1.26.4

Sehingga untuk projek ini **wajib** menggunakan Python **3.9.x**. Disarankan menggunakan Python 3.9.2 – 3.9.13. Python versi tersebut bisa didownload di https://www.python.org/downloads/

### 2. Persiapkan Virtual Environment
   - Letakkan file2 yang dibutuhkan ke folder projek
   - Buka terminal/command prompt di folder projek
   - Buat virtual environment:
     
     ```
     py -3.9 -m venv mp_env
     ```
   - Aktifkan virtual environment (Windows):
     ```
       mp_env\Scripts\activate
     ```
### 3. Install Library yang Dibutuhkan
   - Jalankan perintah berikut:
     
     ```
      pip install -r requirements.txt
     ```
### 4. Ketentuan data training dan tujuan penggunaan
   - Training dari awal, download atau gunakan kaggle API dari link 
     [dataset ini](https://www.kaggle.com/datasets/kapillondhe/american-sign-language)

   - Jika ingin data siap train, download data test/train yang sudah diekstraksi (keypoint dan label) dari
     [link ini](https://drive.google.com/drive/folders/1-CYIYzcI2VOMf6ESV_ZW5BKrJ6mu2uZ5?usp=sharing)

   - Jika ingin langsung menggunakan model pre-trained, download `model_nn.h5` dan `label_encoder.pickle` dari **repo** ini atau  
     [link ini](https://drive.google.com/drive/folders/1bLMTPYfIp5zfRJIPQUcq3ueDLU05xeTU?usp=sharing)
     
### 5. Menjalankan Project (langsung menggunakan model pre-trained)
   - Pastikan virtual environment sudah aktif.
   - Pastikan sudah ada file `test-MLP.ipynb`, `model_nn.h5`, dan `label_encoder.pickle` di folder projek anda
   - Buka file `test-MLP.ipynb` menggunakan Jupyter Notebook atau Visual Studio Code:
     
     Jika dengan VSCode, ganti kernel ke kernel python virtual env (mp_env) dengan python versi 3.9.x

   - Ikuti langkah-langkah berikut sesuai urutan:
     1. Jalankan Sel 'Import library' dan 'Init Awal'
     2. Jalankan Sel 'Deteksi Realtime' secara berurutan
     3. Pastikan webcam berfungsi agar bisa mendeteksi gestur tangan
     4. Agar deteksi lebih akurat, usahakan tangan terlihat jelas. Buka [file ini](/asl_images/asl_images.md) untuk melihat referensi gerakan tangan ASL alfabet 
     5. Tekan tombol 'q' untuk keluar dari deteksi

### 6. Menonaktifkan Virtual Environment
   - Gunakan perintah ini di command:
     ``` 
     deactivate
     ```   
