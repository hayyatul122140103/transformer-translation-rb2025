# transformer-translation-rb2025
RB 2025/2026 - Transformer Translation Task

# Transformer untuk Mesin Penerjemah (English → French)

## Anggota Kelompok
- Hayyatul Fajri (122140103)
- Muhammad Fasya Attoriq (122140107)

## Deskripsi
Tugas ini merupakan eksplorasi pelatihan arsitektur **Transformer** untuk mesin penerjemah dari bahasa **Inggris ke Prancis**.  
Pelatihan dilakukan hanya **1 epoch** dengan **batch size maksimal 100**, sesuai instruksi tugas RB 2025/2026.

## Dataset
- Menggunakan pasangan kalimat dari file:
  - `small_vocab_en.csv` (bahasa Inggris)
  - `small_vocab_fr.csv` (bahasa Prancis)
- Total data: ~5.000 pasangan kalimat
- Preprocessing: lowercase, cleaning karakter non-alfanumerik, tokenisasi whitespace

## Arsitektur Model
- **Model**: Transformer dari `torch.nn`
- **Embedding dim**: 128
- **Attention heads**: 4
- **Encoder/Decoder layers**: 2
- **Positional Encoding**: sinusoidal
- **Vocabulary size**: ~5.000 kata per bahasa

## Proses Pelatihan
- **Loss function**: CrossEntropyLoss (ignore padding)
- **Optimizer**: Adam (lr=0.001)
- **Device**: CPU (Google Colab)
- **Monitoring**: `TrainLoss`, `ValLoss`, dan `ValACC` ditampilkan **setiap akhir batch**

## Inferensi
- Model mampu menerjemahkan kalimat pendek (misal: "hello" → "bonjour")
- Proses decoding: greedy search (tanpa beam search)

