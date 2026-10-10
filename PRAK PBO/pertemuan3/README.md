# Laporan Praktikum 03: Class `RekeningBank` (Java & PHP)

| Keterangan | Detail |
|---|---|
| Nama | Nevilla Ghilar Apryanti |
| NPM | 4525210054 |
| Kelas | PBO A 2025/2026 |
| Mata Kuliah | Pemrograman Berorientasi Objek |
| Dosen Pengampu | Adi Wahyu Pribadi, S.Si., M.Kom. |

## 1. Ringkasan Soal

Praktikum 3 membahas penerapan class, object, constructor, encapsulation, dan anggota static dalam pemrograman berorientasi objek menggunakan Java dan PHP.

Program yang dibuat adalah class `RekeningBank` dengan ketentuan sebagai berikut:

- Nomor rekening bersifat tetap (*immutable*) dan tidak boleh kosong.
- Saldo tidak boleh bernilai negatif.
- Setor dan tarik tunai hanya menerima jumlah positif.
- Bunga tahunan sebesar 2,5%.
- Biaya administrasi sebesar Rp5.000.
- Batas maksimal penarikan sebesar Rp5.000.000.
- Menggunakan constructor delegation untuk mengatur pembuatan objek.
- Menggunakan penghitung jumlah rekening dengan anggota `static`.
- Menyediakan fungsi untuk menghitung bunga tahunan.

## 2. Implementasi Java

Implementasi Java menggunakan dua file, yaitu `RekeningBank.java` sebagai class utama dan `Main.java` sebagai program untuk menjalankan serta menguji class tersebut.

### A. File `RekeningBank.java`

File ini berisi class `RekeningBank` yang mengatur data dan operasi rekening bank. Nomor rekening dibuat tetap, sedangkan saldo dikelola melalui method setor dan tarik.

Perubahan yang diterapkan meliputi validasi nomor rekening, pencegahan saldo negatif, validasi jumlah transaksi, biaya administrasi, batas penarikan, constructor delegation, penghitung jumlah rekening, dan perhitungan bunga tahunan.

**Kode sebelum perbaikan:**

[RekeningBank.java(before)](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan3/java/RekeningBank.java)

**Kode setelah perbaikan:**
[RekeningBank.java(after)](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan3/src/RekeningBank.java)

### B. File `Main.java`

File ini digunakan untuk membuat objek rekening bank dan menjalankan pengujian terhadap method yang tersedia pada class `RekeningBank`.

Pengujian dilakukan untuk melihat proses transaksi, perubahan saldo, jumlah rekening yang dibuat, dan perhitungan bunga tahunan.

**Kode sebelum perbaikan:**

[Main.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan3/java/Main.java)

**Kode setelah perbaikan:**

[RekeningBank.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan3/src/java/Main.java)

## 3. Implementasi PHP

Implementasi PHP menggunakan dua file, yaitu `RekeningBank.php` sebagai class utama dan `main.php` untuk menjalankan program.

### A. File `RekeningBank.php`

File ini berisi class `RekeningBank` dengan fungsi yang serupa dengan implementasi Java. Class ini mengatur nomor rekening, saldo, transaksi setor dan tarik, biaya administrasi, batas penarikan, jumlah rekening, serta perhitungan bunga tahunan.

**Kode sebelum perbaikan:**

[Tautan kode sebelum perbaikan `RekeningBank.php`](#)

**Kode setelah perbaikan:**

[Tautan kode setelah perbaikan `RekeningBank.php`](#)

### B. File `main.php`

File ini digunakan untuk membuat objek `RekeningBank` dan menguji fitur yang telah dibuat pada file `RekeningBank.php`.

Pengujian dilakukan untuk memastikan transaksi berjalan sesuai ketentuan dan data yang tidak valid ditangani dengan benar.

**Kode sebelum perbaikan:**

[Tautan kode sebelum perbaikan `main.php`](#)

**Kode setelah perbaikan:**

[Tautan kode setelah perbaikan `main.php`](#)

## 4. Bukti Eksekusi

### A. Eksekusi Java

**Sebelum perbaikan**

Masukkan screenshot hasil eksekusi Java sebelum perbaikan di sini.

![Output Java sebelum perbaikan](screenshots/java-before.png)

**Sesudah perbaikan**

Masukkan screenshot hasil eksekusi Java setelah perbaikan di sini.

![Output Java setelah perbaikan](screenshots/java-after.png)

### B. Eksekusi PHP

**Sebelum perbaikan**

Masukkan screenshot hasil eksekusi PHP sebelum perbaikan di sini.

![Output PHP sebelum perbaikan](screenshots/php-before.png)

**Sesudah perbaikan**

Masukkan screenshot hasil eksekusi PHP setelah perbaikan di sini.

![Output PHP setelah perbaikan](screenshots/php-after.png)

## 5. Kesimpulan

Berdasarkan praktikum yang telah dilakukan, class `RekeningBank` dapat digunakan untuk menerapkan konsep pemrograman berorientasi objek pada Java dan PHP. Program menerapkan enkapsulasi, constructor delegation, anggota static, serta validasi transaksi agar data rekening tetap sesuai ketentuan.

Melalui praktikum ini, saya memahami cara mengelola data rekening, melakukan transaksi dengan validasi, menghitung bunga tahunan, dan membatasi penarikan agar saldo tidak menjadi negatif.
