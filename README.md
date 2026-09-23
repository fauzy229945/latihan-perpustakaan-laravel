# Sistem Informasi Perpustakaan
Aplikasi pencatatan buku, anggota, dan transaksi peminjaman berbasis Laravel 11.
## Fitur
- CRUD data buku
- CRUD data anggota
- Pencatatan peminjaman & pengembalian buku dengan validasi stok otomatis
## Cara Instalasi
1. Clone repo: `git clone <url-repo>`
2. `composer install`
3. Salin `.env.example` menjadi `.env`, atur koneksi database
4. `php artisan key:generate`
5. `php artisan migrate`
6. `php artisan serve`
## Struktur Folder Penting
- `app/Models` — Buku, Anggota, Peminjaman (berisi logika stok)
- `app/Http/Controllers` — BukuController, AnggotaController, PeminjamanController
- `app/Http/Requests` — validasi form
- `resources/views` — tampilan Blade per modul
## Daftar Halaman/Rute
| Rute | Fungsi |
|---|---|
| `/buku` | Daftar & kelola buku |
| `/anggota` | Daftar & kelola anggota |
| `/peminjaman` | Daftar transaksi + catat peminjaman baru |
| `/peminjaman/{id}/kembalikan` | Tandai buku sudah dikembalikan (stok bertambah) |