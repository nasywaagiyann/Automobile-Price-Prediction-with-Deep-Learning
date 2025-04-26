# Deep Learning Regression - Automobile Price Prediction

## 📄 Deskripsi Proyek
Proyek ini bertujuan untuk membangun model regresi menggunakan Artificial Neural Network (ANN) untuk memprediksi harga mobil berdasarkan berbagai fitur seperti spesifikasi teknis dan karakteristik kendaraan. Model dikembangkan dengan TensorFlow dan Keras.

## 🧰 Tools & Library
- Python
- Pandas, NumPy, Matplotlib, Seaborn, Missingno
- Scikit-learn (preprocessing, train_test_split)
- TensorFlow & Keras

## 📚 Alur Pengerjaan
1. **Impor Library**  
   Menggunakan library standar untuk data handling, visualisasi, preprocessing, dan deep learning.

2. **Memuat Dataset**  
   Dataset _Automobile_data.csv_ dimuat dan dilakukan pemeriksaan struktur data.

3. **Exploratory Data Analysis (EDA)**  
   - Melihat struktur data, statistik deskriptif.
   - Menangani missing values:
     - Mean imputasi untuk data numerik dengan missing < 75%.
     - Modus imputasi untuk data kategorikal.
     - Menghapus kolom jika missing > 75% (tidak ada pada kasus ini).

4. **Feature Engineering**  
   - Label Encoding untuk fitur kategorikal.
   - StandardScaler untuk normalisasi fitur numerik.
   - Membagi dataset menjadi data latih dan data uji (80:20).

5. **Modeling**  
   - Arsitektur ANN dengan beberapa layer Dense, Batch Normalization, dan Dropout.
   - Optimizer: Adam dengan learning rate 0.001.
   - Loss function: Mean Squared Error (MSE).
   - Monitoring model menggunakan EarlyStopping dan ModelCheckpoint.

6. **Evaluasi Model**  
   - Model dievaluasi menggunakan test set.
   - Metrik yang digunakan: Loss (MSE) dan MAE (Mean Absolute Error).

7. **Inference (Prediksi Data Baru)**  
   - Melakukan encoding dan scaling pada input baru sebelum diprediksi.
   - Menghasilkan output prediksi harga mobil.

## 📊 Hasil
- **Test Loss (MSE):** ~2529.8472
- **Test MAE:** ~32.6620
- Model menunjukkan performa yang cukup baik dengan error rata-rata ±33 satuan harga.
