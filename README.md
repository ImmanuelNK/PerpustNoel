📚 Perpustakaan Noel

Sistem Informasi Perpustakaan Berbasis Web menggunakan Laravel

📝 Deskripsi Proyek

Perpustakaan Noel adalah aplikasi web berbasis Laravel yang digunakan untuk mengelola data buku, anggota, serta proses peminjaman dan pengembalian buku.
Aplikasi ini menerapkan sistem Role Based Access Control dengan dua jenis pengguna:

Admin (Petugas) → Mengelola buku, member, dan transaksi

Member (Anggota) → Melihat katalog buku

Sistem ini dirancang untuk menggantikan pencatatan manual menjadi sistem digital yang lebih cepat, aman, dan akurat.

🎯 Fitur Utama
👨‍💼 Admin

Login Admin

Tambah Member

Melihat daftar buku

Input peminjaman buku

Proses pengembalian buku

Stok buku otomatis berkurang dan bertambah

Melihat statistik jumlah buku, member, dan buku yang sedang dipinjam

👤 Member

Login Member

Melihat katalog buku

Melihat stok buku

🗃️ Struktur Database

Sistem menggunakan 3 tabel utama:

Tabel	Fungsi
users	Menyimpan data admin dan member
books	Menyimpan data buku
pinjams	Menyimpan transaksi peminjaman

Relasi utama:

1 User → Banyak Pinjam

1 Book → Banyak Pinjam

Tabel pinjams menjadi penghubung antara user dan buku.

⚙️ Teknologi yang Digunakan

Laravel 10+

PHP 8+

MySQL

Tailwind CSS

Carbon (manajemen tanggal)

Blade Template
