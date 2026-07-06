# CrackMe 01

## 🔬 Informasi Challenge
* **Nama Challenge :** CrackMe 01
* **Sumber :** crackmes.one
* **Tingkat Kesulitan :** Beginner

## 🎯 Tujuan
Mempelajari proses analisis binary menggunakan tools Reverse Engineering untuk memahami logika program.

## 🛠️ Tools yang Digunakan
* Ghidra
* x64dbg
* Detect It Easy (DIE)

## 💻 Langkah Analisis
1. Membuka file menggunakan Detect It Easy untuk melihat informasi dasar file (arsitektur file dan proteksi/packer).
2. Melakukan analisis statis menggunakan Ghidra untuk melihat decompile kode C/C++.
3. Mengidentifikasi fungsi utama program (`main` atau `WinMain`).
4. Mengamati string yang terdapat di dalam binary (mencari string referensi seperti pesan sukses/gagal).
5. Mendokumentasikan hasil analisis.

## 📊 Hasil Analisis & Temuan
* **Analisis Statis (Ghidra):** Pada fungsi utama, teridentifikasi bahwa program menggunakan fungsi perbandingan string standar (`strcmp` / `strncmp`) untuk memvalidasi input dari user.
* **Analisis Dinamis (x64dbg):** Ditemukan instruksi perbandingan logika `CMP` di alamat memori tertentu, diikuti dengan conditional jump `JNZ` / `JZ` yang menentukan apakah alur program lompat ke pesan "Wrong Password" atau tidak.
* **Password/Flag yang Ditemukan:** `[Tulis Password/Key hasil crack-an lu di sini, misal: password123 atau flag{easy_pe}]`

## 📝 Kesimpulan
Challenge ini membantu memahami proses dasar analisis binary serta alur logika percabangan conditional jump sebagai latihan awal Reverse Engineering.
