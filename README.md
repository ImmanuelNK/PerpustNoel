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

👨‍💼 Admin Dashboard

Admin has full control over the system.
Admin Features
Manage Members
Manage Books
Manage Borrowing Transactions
Handle Returns
View Statistics

📊 Dashboard Statistics

Admin can view:
Total Books
Total Members
Books Currently Borrowed

➕ Borrow Book (Pinjam)

Flow
Select Member
Select Book
Click Simpan
System Logic
tanggal_pinjam = NOW()
tanggal_batas = tanggal_pinjam + 7 days
status = "dipinjam"
Book stock is reduced by 1

🔁 Return Book (Kembali)

Flow
Admin clicks Dikembalikan
System Logic
status = "kembali"
tanggal_kembali = NOW()
Book stock increases by 1
The system prevents:
Returning the same book twice

👥 Member Management

Admin can:
Add new members
Each member is stored in users table with role = member

👤 Member Dashboard
Members have read-only access.

📚 Book Catalog

Members can:
View list of books
View author
View stock availability

Members cannot:
Borrow
Return
Edit data

🗃️ Database Design
Tables
Table	Description
users	Stores admin and member accounts
book	Stores book data
pinjam	Stores borrowing transactions

Relationships

User → Pinjam : One to Many
Book → Pinjam : One to Many

🧪 Testing

The system includes Laravel Feature Tests to validate:

Admin can borrow books
Stock cannot go below zero
Admin can return books
Books cannot be returned twice

🔑 Default Login

Admin
Email: admin@noel.com
Password: admin123

Member
Email: krissianto@noel.com
Password: kris123

👤 Author
Immanuel Nissi Krissianto
noelnissi33@gmail.com
