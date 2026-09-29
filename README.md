# Dashboard Siswa Multi-User

Aplikasi web dashboard untuk memonitor data siswa, nilai, dan kehadiran.
Mendukung autentikasi multi-user dengan dua peran pengguna: **Guru** dan **Siswa**.

---

## Berkas yang Dibutuhkan

```
developer/
├── index.html                                    ← Aplikasi utama
├── Master_Data_Dashboard_Siswa_Multi_User.xlsx   ← Basis data (Excel)
└── README.md                                     ← Dokumentasi ini
```

Pastikan seluruh berkas berada dalam **satu folder yang sama**.

---

## ⚠️ Peringatan Sebelum Menjalankan

Perintah pada dokumentasi ini menggunakan contoh lokasi folder berikut:

```
C:\Users\Stefanie\Downloads\developer
```

> **Penting:** Path di atas merupakan contoh dari lingkungan pengembangan
> asli. Apabila Anda menyimpan folder proyek ini di lokasi yang berbeda
> (misalnya di `D:\`, `Documents\`, flash drive, atau folder lain),
> **wajib menyesuaikan perintah `cd`** dengan lokasi folder proyek Anda.

### Contoh Penyesuaian Path

| Lokasi Folder Anda | Perintah `cd` yang Digunakan |
|---------------------|------------------------------|
| `C:\Users\Stefanie\Downloads\developer` | `cd C:\Users\Stefanie\Downloads\developer` |
| `D:\Project\Dashboard` | `cd D:\Project\Dashboard` |
| `C:\Users\NamaAnda\Documents\developer` | `cd C:\Users\NamaAnda\Documents\developer` |
| `E:\Kuliah\Semester5\developer` | `cd E:\Kuliah\Semester5\developer` |

**Tips menemukan path folder Anda:**
1. Buka folder proyek di File Explorer
2. Klik pada kolom **address bar** di bagian atas
3. Path lengkap akan muncul — copy dan gunakan setelah perintah `cd`

---

## Cara Menjalankan

### 1. Buka Command Prompt
Tekan `Win + R` → ketik `cmd` → Enter

### 2. Masuk ke folder proyek
Sesuaikan perintah berikut dengan lokasi folder proyek Anda:

```cmd
cd C:\Users\Stefanie\Downloads\developer
```

> Apabila folder proyek Anda berada di lokasi lain, ganti path di atas
> dengan path folder proyek Anda. (Lihat tabel penyesuaian path di atas.)

### 3. Jalankan web server
```cmd
python -m http.server 8000
```

> Apabila muncul pesan `Serving HTTP on :: port 8000...` → server **berhasil dijalankan**.
> Biarkan jendela ini **tetap terbuka** selama aplikasi digunakan.

### 4. Buka browser
Buka Chrome / Edge, lalu ketik alamat berikut pada address bar:
```
http://localhost:8000
```

### 5. Login

| Peran | Username  | Password   |
|-------|-----------|------------|
| Guru  | guru001   | Guru@123   |
| Siswa | siswa001  | Siswa@001  |

### 6. Mengakhiri sesi
Kembali ke Command Prompt → tekan `Ctrl + C` untuk mematikan server.

---

## Catatan Penting

- **Jangan** membuka `index.html` dengan **double-click** — aplikasi tidak akan berjalan.
- Aplikasi **wajib** diakses melalui `http://localhost:8000`.
- Apabila perintah `python` tidak dikenali, lakukan instalasi Python dari
  https://www.python.org/downloads/ dan **centang opsi "Add Python to PATH"**
  saat proses instalasi.
- Apabila port 8000 sudah digunakan, gunakan port alternatif:
  `python -m http.server 8080` lalu akses `http://localhost:8080`.
- **Pastikan seluruh berkas (`index.html` dan file Excel) berada dalam satu folder
  yang sama.** Apabila file Excel dipindahkan, aplikasi tidak akan dapat membaca data.

---

## Fitur Aplikasi

**Peran Guru:**
- Panel ringkasan (filter tanggal, total siswa, jumlah hadir, tidak hadir, rata-rata nilai)
- Grafik kehadiran, jenis kelamin, distribusi nilai, mata pelajaran favorit, dan ekstrakurikuler
- Pencarian nama / ID siswa
- Filter jenis kelamin
- Tabel data siswa beserta halaman detail
- Timeline riwayat absensi

**Peran Siswa:**
- Profil pribadi (nilai, kelas, jenis kelamin, mata pelajaran favorit, ekstrakurikuler)
- Rekapitulasi kehadiran pribadi
- Timeline riwayat absensi

**Umum:**
- Autentikasi multi-user dengan proteksi akses berbasis peran
- Desain responsif (desktop, tablet, mobile)
- Tampilan modern dengan visualisasi data interaktif

---

## Pengujian Tampilan Mobile

Buka `http://localhost:8000` di Chrome → tekan `F12` → `Ctrl + Shift + M`
untuk menampilkan mode tampilan mobile pada desktop.

Alternatif lain, akses langsung dari perangkat mobile dengan mengganti
`localhost` menjadi **IP komputer** (contoh: `http://192.168.1.10:8000`).