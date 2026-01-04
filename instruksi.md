## INSTRUKSI

**1. Persiapkan Virtual Environment**
   - Pastikan Python terinstal di komputer.
   - Buka terminal/command prompt di folder proyek
   - Buat virtual environment:
     
     ```
     python -m venv mp_env
     ```
   - Aktifkan virtual environment (Windows):
     ```
       mp_env\Scripts\activate
     ```
**2. Install Library yang Dibutuhkan**
   - Jalankan perintah berikut secara berurutan:
     
     ```
     pip install tensorflow==2.15.0      
     pip install mediapipe==0.10.14 protobuf==4.25.3 tqdm scikit-learn opencv-python
     ```
**3. Ketentuan data training dan tujuan penggunaan**
   - Jika ingin melakukan ekstraksi dan training dari awal, download atau gunakan kaggle API dari link 
     [dataset ini](https://www.kaggle.com/datasets/kapillondhe/american-sign-language)

   - Jika ingin data siap train, download data test/train yang sudah diekstraksi (keypoint dan label) dari
     [link ini](https://drive.google.com/drive/folders/1-CYIYzcI2VOMf6ESV_ZW5BKrJ6mu2uZ5?usp=sharing)

   - Jika ingin langsung menggunakan model pre-trained, download `model_nn.h5` dan `label_encoder.pickle` dari repo ini atau  
     [link ini](https://drive.google.com/drive/folders/1bLMTPYfIp5zfRJIPQUcq3ueDLU05xeTU?usp=sharing)
     
**4. Menjalankan Project (untuk model pretrained)**
   - Pastikan virtual environment sudah aktif.
   - Buka file `test-MLP.ipynb` menggunakan Jupyter Notebook atau Visual Studio Code:
     
     Jika dengan VSCode, ganti kernel ke kernel python virtual env (mp_env)

   - Ikuti langkah-langkah berikut sesuai urutan:
     1. Jalankan Sel 'Import library' dan 'Init Awal'
     2. Pastikan sudah ada file `model_nn.h5` dan `label_encoder.pickle` di folder projek anda
     3. Jalankan Sel 'Deteksi Realtime' secara berurutan
     4. Pastikan webcam berfungsi agar bisa mendeteksi gestur tangan
     5. Agar deteksi lebih akurat, usahakan tangan terlihat jelas. Buka [file ini](/docs/asl_images.md) untuk melihat referensi gerakan tangan ASL alfabet 
     6. Tekan tombol 'q' untuk keluar dari deteksi

**5. Menonaktifkan Virtual Environment**
   - Gunakan perintah ini di command:
     ``` 
     deactivate
     ```   
