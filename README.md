# Studi Ablasi RNN, LSTM, GRU vs ANN untuk Prediksi Trafik Seluler Milan

Tugas Workshop Deep Learning — Teknik Telekomunikasi ITERA.

<!-- Ganti seluruh isian bertanda [ ... ] di bawah. Hapus komentar ini. -->

## Kelompok

| Peran | Nama | NIM |
|---|---|---|
| Ketua | [Rossa Amelia putri] | [124400032] |
| Anggota | [Eliada Marcela Bangun] | [124400044] |
| Anggota | [Tino Sumandi Siregar] | [124400036] |

- **Kelas:** [RB]
- **Lokasi kelompok:** [2] — [Universitas Bocconi]
- **Laporan:** [`laporan-latex/main.pdf`]

## Cara Menjalankan

```bash
uv sync
uv run jupyter lab
```

Buka `tugas_ablasi.ipynb`, isi `LOKASI_KELOMPOK`, lalu jalankan semua sel. Semua run tercatat di `hasil/ablasi.csv`.

Perangkat yang kami pakai: [contoh: laptop CPU Intel i5 / Google Colab T4], total waktu training: [x] menit.

## Ringkasan Hasil

Hasil eksperimen menunjukkan bahwa konfigurasi terbaik yang dipilih berdasarkan validation MAE mampu meningkatkan kinerja seluruh model dibandingkan konfigurasi acuan. Nilai test MAE pada konfigurasi terpilih masing-masing adalah ANN 269,4; RNN 224,5; LSTM 245,6; dan GRU 220,3. Model GRU menghasilkan performa terbaik pada data pengujian dengan test MAE terendah sebesar 220,3, sedangkan pada periode Natal, RNN menunjukkan kemampuan generalisasi terbaik dengan MAE sebesar 404,5.

## Struktur

```
tugas_ablasi.ipynb      notebook eksperimen (di-commit beserta output)
data/                   data trafik per jam (Duomo + 10 lokasi tugas)
hasil/                  CSV seluruh run, tabel, dan grafik
laporan-latex/ atau laporan-typst/   sumber laporan + PDF
```

## Data

Telecom Italia Big Data Challenge (Barlacchi dkk., 2015, *Scientific Data*, lisensi ODbL), versi per jam dari Zhang dkk. (INFOCOM 2021). Disiapkan oleh pengajar di repo [mctosima/dl-workshop](https://github.com/mctosima/dl-workshop).
