# 🩺 Sistem Pakar Diagnosa Penyakit Kolesterol

> Program berbasis **Certainty Factor** untuk mendiagnosa jenis penyakit kolesterol melalui serangkaian pertanyaan gejala klinis.

![C++](https://img.shields.io/badge/Language-C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

---

## 📌 Deskripsi

Program ini merupakan implementasi **Sistem Pakar (Expert System)** untuk mendiagnosa penyakit kolesterol menggunakan metode **Certainty Factor (CF)**. Sistem akan mengajukan **8 pertanyaan gejala** kepada pengguna dengan skala keyakinan 1–5, lalu menghitung nilai CF secara kombinatif untuk menentukan apakah pengguna mengidap **Kolesterol Baik (HDL)** atau **Kolesterol Jahat (LDL)**, beserta tingkat keyakinannya dalam bentuk persentase.

Program ini dibuat sebagai tugas mata kuliah **Kecerdasan Buatan (Artificial Intelligence)** di Universitas Sriwijaya.

---

## ✨ Fitur

- 🔍 Diagnosa berbasis 8 gejala klinis kolesterol
- 📊 Perhitungan nilai Certainty Factor secara otomatis
- 🎯 Output diagnosis: **Kolesterol Baik** atau **Kolesterol Jahat** + persentase keyakinan
- 💊 Rekomendasi tindakan kesehatan pasca-diagnosa
- 🔁 Opsi mengulang diagnosa untuk pengguna berbeda
- 🎨 Tampilan konsol berwarna untuk UX yang lebih baik

---

## 🧠 Metode: Certainty Factor

**Certainty Factor (CF)** adalah metode yang digunakan dalam sistem pakar untuk menangani ketidakpastian dalam proses pengambilan keputusan. Nilai CF dihitung secara kombinatif menggunakan formula:

```
CF_combined = CF1 + (CF2 × (1 - CF1))
```

### Skala Input Pengguna

| Pilihan | Keterangan | Nilai CF |
|:---:|---|:---:|
| 1 | Tidak Benar | 0.0 |
| 2 | Kurang Yakin | 0.2 |
| 3 | Kemungkinan Kecil | 0.5 |
| 4 | Kemungkinan Besar | 0.8 |
| 5 | Sangat Yakin | 1.0 |

### Gejala & Bobot CF

| No | Gejala | Bobot CF | Terkait |
|:---:|---|:---:|---|
| G01 | Nyeri pada kaki dan kram di malam hari | 0.60 | HDL & LDL |
| G02 | Kesemutan | 0.05 | HDL & LDL |
| G03 | Sakit kepala | 0.25 | HDL & LDL |
| G04 | Gampang mengantuk | 0.05 | HDL & LDL |
| G05 | Pegal-pegal sampai ke pundak | 0.25 | HDL & LDL |
| G06 | Mudah kelelahan | 0.10 | LDL |
| G07 | Daerah tengkuk belakang sakit sampai kepala | 0.60 | LDL |
| G08 | Kelebihan berat badan | 0.05 | LDL |

### Hasil Diagnosa

| Kondisi | Diagnosa |
|---|---|
| Nilai CF ≤ 0.5 | Tidak mengidap penyakit kolesterol |
| CF Kolesterol Baik > CF Kolesterol Jahat | **Kolesterol Baik (HDL)** |
| CF Kolesterol Jahat > CF Kolesterol Baik | **Kolesterol Jahat (LDL)** |

---

## 🖥️ Tampilan Program

```
:=================================================================================================:
|>>>>>>> SISTEM PAKAR DIAGNOSA PENYAKIT KOLESTEROL MENGGUNAKAN METODE CERTAINLY FACTOR <<<<<<<<<<<|
|                                                                                                 |
|                                       FAISHAL FITRA RAMADHAN                                    |
|                            KECERDASAN BUATAN (ARTIFICIAL INTELLIGENCE)                          |
|                                                                                                 |
:=================================================================================================:
|                 - SELAMAT DATANG DI SISTEM PAKAR DIAGNOSA PENYAKIT KOLESTEROL -                 |
|_________________________________________________________________________________________________|
|                                     - METODE CERTAINLY FACTOR -                                 |
:=================================================================================================:

 Masukkan Nama Lengkap Anda  = Budi Santoso
 Masukkan Gender Anda [L/P]  = L

 Hallo Saudara Budi Santoso , Selamat Datang Di Sistem Pakar Diagnosa Penyakit Kolesterol.
```

---

## ⚙️ Cara Menjalankan

### Prasyarat

- Sistem Operasi: **Windows** (program menggunakan `windows.h` dan `conio.h`)
- Compiler: **MinGW / g++** atau **Dev-C++** / **Code::Blocks**

### Langkah Kompilasi & Eksekusi

**Menggunakan g++ (MinGW):**
```bash
# Clone repository
git clone https://github.com/faishalfitrar/sistem-pakar-kolesterol.git
cd sistem-pakar-kolesterol

# Kompilasi
g++ -o sistem_pakar_kolesterol sistem_pakar_kolesterol.cpp

# Jalankan
./sistem_pakar_kolesterol.exe
```

**Menggunakan Dev-C++ / Code::Blocks:**
1. Buka file `sistem_pakar_kolesterol.cpp`
2. Tekan **F11** (Build & Run) di Dev-C++ atau **F9** di Code::Blocks

### Alur Penggunaan

1. Masukkan **nama lengkap** pengguna
2. Masukkan **gender** [L/P]
3. Jawab **8 pertanyaan gejala** dengan skala 1–5
4. Sistem menampilkan **hasil diagnosa** dan **rekomendasi**
5. Pilih apakah ingin **mengulang** diagnosa [y/n]

---

## 📁 Struktur Repository

```
sistem-pakar-kolesterol/
├── sistem_pakar_kolesterol.cpp   # Source code utama
└── README.md                     # Dokumentasi proyek
```

---

## 📚 Referensi

- Shortliffe, E.H. & Buchanan, B.G. (1975). *A Model of Inexact Reasoning in Medicine* — Makalah asli yang memperkenalkan metode Certainty Factor.
- Kusumadewi, S. (2003). *Artificial Intelligence: Teknik dan Aplikasinya*. Graha Ilmu.

---

## 👤 Author

**Faishal Fitra Ramadhan**
- GitHub: [@faishalfitrar](https://github.com/faishalfitrar)
- LinkedIn: [faishalfitrar](https://linkedin.com/in/faishalfitrar)
- Email: faishalfitraramadhan01@gmail.com

---

## ⚠️ Disclaimer

Program ini dibuat untuk keperluan **akademik** dan **demonstrasi konsep sistem pakar**. Hasil diagnosa **tidak menggantikan** konsultasi dengan tenaga medis profesional. Selalu konsultasikan kondisi kesehatan Anda kepada dokter.

---

> ⭐ Jika proyek ini bermanfaat, jangan lupa beri **star** pada repository ini!
