# mzgentrial
📌 PendahuluanMANZAX GENERATOR adalah script untuk membuat akun Free Fire (Garena) secara otomatis dengan kecepatan tinggi (hingga 3000 thread, 3 detik timeout, 100 ribu IP).Versi ini sudah dienkripsi agar source code tidak terbaca, cocok untuk dijual atau dibagikan secara terbatas.
# 📘 README – MANZAX GENERATOR (OB54 ULTRA SPEED)
============================================
# 🔐 Bagian 1: Membuat File Terenkripsi (Untuk Penjual)
Langkah ini hanya dilakukan sekali oleh penjual untuk menghasilkan file manzax_encrypted.py yang siap diberikan ke pembeli.

1.1 Siapkan file source
Pastikan Anda memiliki file manzax_full.py (gabungan wrapper + engine) di direktori yang sama.

1.2 Buat file encrypt.py
bash
nano encrypt.py
Isi dengan:

import zlib, base64

with open('manzax_full.py', 'r') as f:
    source = f.read()

compressed = zlib.compress(source.encode())
encoded = base64.b64encode(compressed).decode()

stub = f'''#!/usr/bin/env python3
import zlib, base64, os
exec(zlib.decompress(base64.b64decode("{encoded}")))
'''

with open('manzax_encrypted.py', 'w') as f:
    f.write(stub)

print("✅ manzax_encrypted.py berhasil dibuat!")

Simpan (Ctrl+O, enter,X Enter).

1.3 Jalankan builder
bash
python encrypt.py
Maka akan muncul file manzax_encrypted.py – inilah file yang akan Anda berikan ke pembeli.
============================================

# 🔑 Bagian 2: Membuat Support Key (Untuk Penjual)
Support key adalah kunci yang harus dimasukkan pembeli saat menjalankan script. Tanpa key, script tidak jalan.

2.1 Buat file manzax_keymaker.py
bash
nano manzax_keymaker.py
Isi dengan kode keymaker yang sudah saya berikan sebelumnya (atau Anda bisa copy dari jawaban sebelumnya).

2.2 Jalankan keymaker
bash
python manzax_keymaker.py
Pilih menu 1 → masukkan User ID (bisa nama pembeli) → tentukan durasi (hari) → dapatkan support key.
Contoh key:
MANZAX-joko123-1a2b3c4d5e6f-1734567890-abc123

2.3 Kirimkan ke pembeli
File manzax_encrypted.py

Support key yang sudah digenerate

Instruksi di bawah ini

============================================

# 📦 Bagian 3: Panduan untuk Pembeli (Pengguna Akhir)
3.1 Persyaratan
Termux (Android) atau Linux

Python 3.7+

Koneksi internet

3.2 Instalasi di Termux
bash
pkg update && pkg upgrade -y
pkg install python -y
pip install --upgrade pip
pip install pycryptodome requests colorama
3.3 Letakkan file
Salin file manzax_encrypted.py ke direktori Termux (misal di ~/storage/downloads atau /sdcard).

3.4 Jalankan
bash
python manzax_encrypted.py
3.5 Masukkan Support Key
Saat muncul prompt:

text
⚠️ SUPPORT KEY WAJIB DIISI!
KETIK '0' UNTUK CLOSE SEMUA SCRIPT
➜ SUPPORT KEY : 
Paste support key yang Anda terima dari penjual, lalu tekan Enter.

Jika valid, script akan berjalan dan menampilkan menu utama generator.

🛠️ Bagian 4: Troubleshooting
Masalah	Solusi
ModuleNotFoundError: No module named 'Crypto'	Jalankan pip install pycryptodome
ModuleNotFoundError: No module named 'requests'	Jalankan pip install requests
ModuleNotFoundError: No module named 'colorama'	Jalankan pip install colorama
Support key tidak valid	Pastikan key diketik dengan benar (termasuk tanda minus) atau key sudah expired
bash: !/usr/bin/env: event not found	Gunakan metode encrypt.py seperti di atas, jangan pakai perintah satu baris
File tidak ditemukan	Pastikan manzax_encrypted.py berada di direktori yang sama dengan tempat Anda menjalankan python
Error lain	Periksa koneksi internet dan pastikan tidak ada firewall yang memblokir akses ke Garena
📞 Kontak Support
Jika ada kendala, hubungi:
# 📱 Telegram: [@MANZAX_SUPPORT]

# ⚠️ Disclaimer
Script ini dibuat untuk tujuan edukasi. Penggunaan di luar tanggung jawab pengguna.
Pastikan Anda mematuhi kebijakan layanan Garena/Free Fire.

Selamat menggunakan MANZAX GENERATOR! 🚀
