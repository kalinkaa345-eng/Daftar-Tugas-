# Tabel Perbandingan Refactoring

Folder `sebelum_refactoring` dan `sesudah_refactoring` menjalankan alur yang sama: menyaring data, mengurutkan tugas, menampilkan daftar, lalu menyusun laporan. Kedua program menggunakan data contoh yang sama dan menghasilkan keluaran yang sama.

| Bagian yang belum diperbaiki | Bagian yang diperbaiki | Teknik | Alasan |
|---|---|---|---|
| Variabel menggunakan nama pendek seperti `a`, `b`, `c`, dan `d` di `sebelum_refactoring/program.py` | Nama diganti menjadi `daftar_tugas`, `tugas_valid`, dan `jumlah_belum_selesai` di `sesudah_refactoring/program.py` | Rename Variable | Nama variabel menjelaskan isi data. |
| Penyaringan data dan penyusunan laporan berada dalam satu alur panjang | Langkah tersebut dipisah ke fungsi `saring_tugas()` dan `buat_laporan()` | Extract Function | Setiap fungsi mempunyai satu tanggung jawab dan alur utama lebih mudah dibaca. |
| Format satu baris tugas ditulis dua kali, untuk tampilan dan laporan | Fungsi `format_tugas()` membentuk baris yang dipakai pada tampilan dan laporan | Remove Duplicate Code | Satu aturan format dipakai ulang sehingga hasilnya konsisten. |

## Penjelasan singkat

1. **Rename Variable** memperjelas arti nama variabel.
2. **Extract Function** memindahkan pekerjaan tertentu ke fungsi tersendiri.
3. **Remove Duplicate Code** memakai satu fungsi format di dua bagian program.

Ketiga perubahan tersebut menjaga data contoh dan keluaran tetap sama. Program utama yang sudah dirapikan ada di `main.py` dan package `tugas_kuliah`.
