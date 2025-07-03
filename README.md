# Deteksi Emosi Pengguna dari Teks Bahasa Indonesia menggunakan IndoBERT

## 📚 Deskripsi Proyek
Proyek ini merupakan tugas Ujian Akhir Semester dari mata kuliah **Kecerdasan Buatan**.  
Tujuan dari proyek ini adalah membangun sebuah model kecerdasan buatan menggunakan pendekatan **Natural Language Processing (NLP)** untuk **mendeteksi emosi atau mood pengguna berdasarkan teks dalam Bahasa Indonesia**.  
Model yang digunakan adalah **IndoBERT (indobenchmark/indobert-base-p1)**, yaitu model BERT yang sudah dilatih khusus untuk Bahasa Indonesia.

## 👤 Informasi Mahasiswa
- **Nama**: Fauzi Amrul Azmi  
- **NIM**: STI202303559  
- **Mata Kuliah**: Kecerdasan Buatan  
- **Dosen Pengampu** : Ardian Webi Kirda, S.Kom., M.Eng

- Python 3.11
- Google Colab
- HuggingFace Transformers
- scikit-learn
- pandas, numpy, matplotlib
- IndoBERT (`indobenchmark/indobert-base-p1`)

## 🔍 Dataset
Dataset yang digunakan adalah:
> **Indonesian Twitter Emotion Dataset** oleh [meisaputri21](https://github.com/meisaputri21/Indonesian-Twitter-Emotion-Dataset)

Dataset ini terdiri dari ratusan tweet dalam Bahasa Indonesia yang sudah dilabeli dengan 5 kategori emosi:
- `anger`
- `fear`
- `happy`
- `love`
- `sadness`

Dataset digunakan untuk melatih model klasifikasi teks guna mendeteksi emosi pengguna secara otomatis.

## 🧪 Proses Pengerjaan
1. **Pra-pemrosesan data**
   - Pembersihan kolom dan label
   - Label encoding

2. **Tokenisasi**
   - Menggunakan tokenizer dari IndoBERT
   - Padding dan truncation disesuaikan untuk input model BERT

3. **Pelatihan Model**
   - Menggunakan `Trainer` dari HuggingFace
   - Subset 400 data untuk training dan 100 data untuk testing
   - Evaluasi dengan metrik `accuracy` dan `F1-score`

4. **Prediksi**
   - Input teks dari pengguna diproses dan diklasifikasikan ke salah satu dari 5 emosi

