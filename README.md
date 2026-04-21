# ⚡ PerfEngine Pro - Graham Bell 2T/4T + Smart CR

[![Vue.js](https://img.shields.io/badge/Vue.js-3.x-42b883?logo=vue.js)](https://vuejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38bdf8?logo=tailwindcss)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.x-ff6384?logo=chart.js)](https://www.chartjs.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Kalkulator Performa Mesin Profesional** berbasis metode **A. Graham Bell** dengan dukungan penuh untuk mesin **2-Tak & 4-Tak**, **Gasoline & Diesel**, serta fitur **Smart Compression Ratio Recommendation**.

![PerfEngine Pro Screenshot](https://via.placeholder.com/800x400?text=PerfEngine+Pro+Screenshot)

---

## 📋 Daftar Isi

- [✨ Fitur Utama](#-fitur-utama)
- [🚀 Demo Langsung](#-demo-langsung)
- [📦 Instalasi & Penggunaan](#-instalasi--penggunaan)
- [🔧 Panduan Penggunaan](#-panduan-penggunaan)
- [📐 Rumus & Perhitungan](#-rumus--perhitungan)
- [🏍️ Preset Database](#️-preset-database)
- [📁 Struktur Proyek](#-struktur-proyek)
- [🤝 Kontribusi](#-kontribusi)
- [📄 Lisensi](#-lisensi)
- [📞 Kontak & Dukungan](#-kontak--dukungan)

---

## ✨ Fitur Utama

### 🔬 **Kalkulasi Akurat Graham Bell**
- **Compression Ratio (CR)** - Perhitungan presisi dengan chamber, gasket, dan piston dome/dish
- **Swept Volume & Clearance Volume** - Per silinder dan total
- **Estimated Horsepower** - Estimasi HP berdasarkan VE (Volumetric Efficiency)
- **AFR Suggestion** - Rekomendasi Air-Fuel Ratio untuk NA/Turbo
- **Octane/Cetane Rating** - Rekomendasi bahan bakar optimal

### 🧠 **Smart AI Insight**
- Analisis real-time setup mesin
- Rekomendasi perbaikan CR otomatis
- Warning knocking risk & fuel mismatch
- Saran upgrade berbasis data

### 🏍️ **Database Lengkap Motor Indonesia**
| Kategori | Contoh Model |
|----------|-------------|
| Bebek & Underbone | Supra X 125, Jupiter Z, Shogun 125 |
| Matic Entry | BeAT, Mio, Scoopy, Vario 110 |
| Matic & Sport 125-150cc | Vario 125/150, PCX, NMAX, Aerox, CB150R, R15, GSX-R150 |
| Naked & Sport 155-250cc | MT-15, CBR150R, CBR250RR, Ninja 250, Z250 |
| Moge & Touring | MT-25, Versys-X 250, CRF250L, KLX250 |
| Mobil | Avanza, Brio, 1.5 Turbo |
| Diesel | Isuzu 4JB1, Mitsubishi 4D56, Toyota 1KD |

### 🛢️ **Mode Diesel Khusus**
- **Auto-disable preset motor** (diesel = mobil/truk)
- **Engine cycle lock ke 4-Tak**
- **Cetane rating recommendation** (CN 48-55)
- **Target CR 16:1 - 22:1**
- **AFR 18:1 - 25:1 (lean burn)**
- **Preset mesin diesel populer**

### 📊 **Visualisasi Dinamis**
- Grafik HP vs RPM interaktif (Chart.js)
- Perbandingan NA vs Turbo
- VE adjustment otomatis berdasarkan setup
- Responsive untuk mobile & desktop

### 🌓 **Dark Mode & Persistence**
- Toggle dark/light mode
- Auto-save ke localStorage
- Export/Import JSON

---

## 🚀 Demo Langsung

🔗 **[Coba PerfEngine Pro Sekarang](https://squarednalytic.github.io/PerfEngine-Pro/)**

Atau jalankan secara lokal:

```bash
# Clone repository
git clone https://github.com/username/perfengine-pro.git

# Buka file index.html di browser
cd perfengine-pro
open index.html
# atau double-click index.html
🔧 Panduan Penggunaan
1️⃣ Pilih Tipe Mesin
Parameter	Opsi	Keterangan
Fuel	Gasoline / Diesel	Diesel auto-lock ke 4-Tak & Mobil
Engine Cycle	2-Tak / 4-Tak	2-Tak = VE lebih tinggi
Induction	NA / Turbo	Turbo = boost VE & HP
Cylinders	1-12	Multi-silinder support
2️⃣ Masukkan Dimensi
Parameter	Satuan	Contoh
Bore (std)	mm	50.0 (BeAT)
Stroke	mm	55.1
Chamber CC	cc	10.5
Gasket Thick	mm	1.0
Gasket Bore	mm	51.0
Dome/Dish	cc	-1.5 (dome) / +5.0 (dish)
3️⃣ Gunakan Preset (Opsional)

    Pilih dari dropdown "PRESET LENGKAP MOTOR INDONESIA"

    Data bore, stroke, chamber akan terisi otomatis

    Untuk Diesel, gunakan preset di optgroup "DIESEL ENGINES"

4️⃣ Analisis Hasil

    Sticky Result Panel: CR, Safety Label, HP

    AFR & Octane Card: Rekomendasi bahan bakar

    AI Insight: Analisis & saran perbaikan

    HP Chart: Kurva performa NA vs Turbo

5️⃣ Optimasi CR

Jika muncul tombol "💡 Fix to XX":

    Klik untuk otomatis menyesuaikan chamber CC

    Mencapai CR ideal (Gasoline: 10.5:1, Diesel: 18:1)

6️⃣ Simpan & Ekspor

    💾 Save: Simpan state ke localStorage

    📄 JSON: Ekspor data ke file .json

    🔄 Reset: Kembalikan ke default

    🌙 Mode: Toggle dark/light

Octane Requirement (Gasoline)
CR Range	RON	Bahan Bakar
< 9.5	RON 90	Pertalite
9.5 - 10.5	RON 92	Pertamax
10.6 - 11.5	RON 95	Pertamax Turbo
> 11.5	RON 98+	Racing Fuel
Cetane Requirement (Diesel)
CR Range	Cetane	Bahan Bakar
14-16	CN 45+	Solar Biasa
16-18	CN 48-52	Dexlite
> 18	CN 50-55	Pertamina Dex
🏍️ Preset Database
Motor Bebek & Underbone
Model	Bore	Stroke	Cyl	CR
Supra X 125	52.4	57.9	1	9.3
Jupiter Z	51.0	54.0	1	9.3
Shogun 125	53.5	55.2	1	9.6
Matic Entry
Model	Bore	Stroke	Cyl	CR
BeAT / Mio	50.0	55.1	1	9.5
Scoopy 110	50.0	55.6	1	9.5
Vario 110	50.0	55.1	1	9.5
Nex 115	51.0	55.2	1	9.4
Matic & Sport 125-150cc
Model	Bore	Stroke	Cyl	CR
Vario 125	52.4	57.9	1	11.0
Vario 150	57.3	57.8	1	11.0
PCX 150	57.3	57.9	1	10.6
NMAX 155	58.0	58.7	1	11.6
Aerox 155	58.0	58.7	1	11.6
CB150R	57.3	57.8	1	11.3
R15 V4	58.0	58.7	1	11.6
GSX-R150	62.0	48.8	1	11.5
Sport 250cc
Model	Bore	Stroke	Cyl	CR
CBR250RR	62.0	41.4	2	12.5
Ninja 250	62.0	41.2	2	11.3
Z250	62.0	41.2	2	11.3
Diesel
Model	Bore	Stroke	Cyl	CR
Isuzu 4JB1	93.0	102.0	4	18.5
Mitsubishi 4D56	91.1	95.0	4	21.0
Toyota 1KD	96.0	103.0

🤝 Kontribusi

Kontribusi sangat diterima! Berikut cara berkontribusi:
🐛 Bug Report

    Buka Issue dengan deskripsi jelas

    Sertakan screenshot & steps to reproduce

    Sebutkan browser & device yang digunakan

💡 Feature Request

    Jelaskan fitur yang diinginkan

    Berikan use-case atau contoh

    Diskusikan di Discussions terlebih dahulu

🔧 Pull Request

    Fork repository

    Buat branch fitur (git checkout -b feature/AmazingFeature)

    Commit perubahan (git commit -m 'Add some AmazingFeature')

    Push ke branch (git push origin feature/AmazingFeature)

    Buka Pull Request

✅ To-Do List

    Tambah preset motor listrik

    Kalkulator cam duration & lift

    Simulasi turbo compressor map

    Export ke PDF report

    Multi-language support (EN/ID)

📄 Lisensi

Didistribusikan di bawah MIT License. Lihat LICENSE untuk informasi lebih lanjut.
MIT License

Copyright (c) 2024 PerfEngine Pro

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files...
Bebas digunakan untuk:

    ✅ Proyek pribadi & komersial

    ✅ Modifikasi & redistribusi

    ✅ Penggunaan pribadi & profesional

⭐ Ucapan Terima Kasih

    A. Graham Bell - Referensi utama "Performance Tuning in Theory and Practice"

    Vue.js Team - Framework reactive yang powerful

    Tailwind Labs - Utility-first CSS framework

    Chart.js Contributors - Library visualisasi data

    Komunitas Otomotif Indonesia - Data & feedback preset motor

Dibuat dengan ❤️ untuk komunitas otomotif Indonesia

"Performance is not just about horsepower, it's about understanding your engine."
— A. Graham Bell
