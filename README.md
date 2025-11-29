# Yogi-Ferdiansyah-Amta-Miluloh_H1H024027_ResponsiPBO25

# PokéCare – Responsi PBO Teknik Komputer 2025

## Identitas
- Nama                 : Yogi Ferdiansyah Amta Miluloh
- NIM                  : H1H024027
- Shift Responsi Awal  : B
- Shift Responsi Akhir : B

---

## Deskripsi Aplikasi
PokéCare adalah aplikasi berbasis PHP Native yang menerapkan  
4 Pilar OOP dalam konsep pelatihan Pokémon.

Pengguna dapat:
- Melihat status Pokémon
- Melatih Pokémon berdasarkan jenis latihan & intensitas
- Mendapatkan peningkatan Level dan HP
- Melihat riwayat latihan yang sudah dilakukan

UI dibuat kyk konsep animasi dan api

---

## Struktur OOP

| Class | Deskripsi | Penerapan OOP |
|-------|-----------|---------------|
| `Pokemon` (abstract) | Blueprint untuk semua Pokémon | Abstraction |
| `Arcanine` | Pokémon tipe Fire yang mewarisi dari Pokemon | Inheritance + Polymorphism |
| `GameManager` | Mengelola state Pokémon & history | Encapsulation |

### Implementasi 4 Pilar OOP
- Abstraction = `Pokemon` sebagai abstract class
- Encapsulation = properti dibuat `protected/private` + getter/setter
- Inheritance = `class Arcanine extends Pokemon`
- Polymorphism = override `specialMove()` & `train()` untuk tipe Fire

---

## Halaman Utama (index.php)
Fitur:
- Menampilkan:
  - Nama Pokémon
  - Level
  - HP sekarang & maksimal
  - Type Pokémon
  - Jurus spesial
- Tombol:
  - start Training
  - Training History

---

##  Halaman Pelatihan (train.php)
Fitur:
- Pilihan Training Type:
  - Strength → meningkatkan Attack + sedikit HP
  - Speed → meningkatkan Speed + HP sedikit
  - Defense → meningkatkan Defense + HP stabil
- Pilihan Intensity 1–10
- Pokémon akan:
  - Mendapat EXP → Naik Level bila cukup
  - HP bertambah berdasarkan tipe latihan
- Hasil latihan ditampilkan setelah submit
- Riwayat disimpan ke `history.json`

---

## 📜 Halaman Riwayat Latihan (history.php)
Fitur:
- Tabel berisi seluruh sesi latihan:
  - Waktu latihan
  - Jenis latihan
  - Intensitas
  - Level before → after
  - HP before → after
- Scrollable jika data banyak
- Tombol Kembali dan Train Again

---

## struktur file
responsi_pokecare/
│
├── index.php
├── train.php
├── history.php
├── readme.md
│
├── src/
│ ├── Pokemon.php
│ ├── Arcanine.php
│ ├── GameManager.php
│
├── data/
│ ├── pokemon.json
│ └── history.json
│
└── assets/
├── style.css
├── arcanine.png
└── arcanine_wall.png

## cara menjalankan, klo dari github:
- dowload .zip nya (kenapa make zip? ga bisa-bisa jir.. mke akun baru malah ngestuck)]
- extract di folder yg nyambung ama laragon
- import di vs-code kalau mau
- buka laragon
- start + klik kanan + www + pilih foldernya
- masuk browser + pilih folder yg abis di extract tadi
- done, semoga muncul
