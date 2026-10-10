# Laporan Praktikum PBO A — Pertemuan 2
**Nama:** Nevilla Ghilar Apryanti  
**NPM:** 4525210054

## 1. Deskripsi Tugas

Pada Pertemuan 2, tugas membahas enkapsulasi yang menjaga invariant pada class `Mahasiswa`. Program digunakan untuk menyimpan data mahasiswa berupa NIM, nama, nilai tugas, UTS, dan UAS. Nilai akhir dihitung berdasarkan bobot yang telah ditentukan, kemudian dikonversi menjadi huruf mutu.

Program juga menerapkan validasi agar NIM tidak kosong dan setiap komponen nilai berada dalam rentang 0 sampai 100.

## 2. Penjelasan Kode Java

### a. Mahasiswa.java

File `Mahasiswa.java` berisi class `Mahasiswa` yang digunakan untuk menyimpan dan mengelola data mahasiswa.

1) **Konstanta bobot nilai**

   `BOBOT_TUGAS`, `BOBOT_UTS`, dan `BOBOT_UAS` merupakan konstanta yang menentukan bobot nilai tugas sebesar 30%, UTS sebesar 30%, dan UAS sebesar 40%.

2) **Atribut class**

   Atribut `nim` dan `nama` menggunakan `private final` agar nilainya tidak dapat diubah setelah objek dibuat. Sementara itu, atribut nilai tugas, UTS, dan UAS dapat berubah.

3) **Constructor**

   Constructor digunakan untuk mengisi data mahasiswa saat objek dibuat. Constructor memeriksa agar NIM tidak kosong atau `null`, serta memastikan setiap nilai berada dalam rentang 0–100.

4) **Method `pastikanNilaiSah()`**

   Method privat ini digunakan untuk memvalidasi nilai. Jika nilai kurang dari 0 atau lebih dari 100, program akan menghasilkan `IllegalArgumentException`.

5) **Method `nilaiAkhir()`**

   Method ini menghitung nilai akhir berdasarkan bobot tugas 30%, UTS 30%, dan UAS 40%.

6) **Method `hurufMutu()`**

   Method ini menentukan huruf mutu berdasarkan nilai akhir, yaitu A untuk nilai minimal 80, B untuk minimal 70, C untuk minimal 60, D untuk minimal 50, dan E untuk nilai di bawah 50.

7) **Getter**

   Method `getNim()` dan `getNama()` digunakan untuk mengambil data NIM dan nama mahasiswa.

8) **Method `toString()`**

   Method ini mengatur tampilan data mahasiswa agar NIM, nama, nilai akhir, dan huruf mutu dapat ditampilkan dalam bentuk yang rapi.

### b. Main.java

File `Main.java` digunakan untuk menjalankan dan menguji class `Mahasiswa`.

1) Program menampilkan judul **Rekap Nilai**.

2) Program membuat tiga objek mahasiswa, yaitu Ani Lestari, Budi Santoso, dan Citra Wijaya, beserta nilai tugas, UTS, dan UAS masing-masing.

3) Perulangan `for` digunakan untuk menampilkan data setiap mahasiswa melalui method `toString()`.

4) Program menguji validasi nilai dengan membuat objek yang memiliki nilai tugas 150. Data tersebut seharusnya ditolak karena melebihi batas maksimal 100.

5) Program menguji validasi NIM kosong. Jika terjadi kesalahan, program menangkap `IllegalArgumentException` dan menampilkan pesan penolakan.

## 3. Penjelasan Kode PHP

### a. Mahasiswa.php

File `Mahasiswa.php` merupakan implementasi class `Mahasiswa` menggunakan bahasa PHP dengan fungsi yang setara dengan versi Java.

1) **Konstanta bobot nilai**

   Konstanta `BOBOT_TUGAS`, `BOBOT_UTS`, dan `BOBOT_UAS` digunakan untuk menentukan bobot setiap komponen nilai.

2) **Atribut class**

   Atribut NIM dan nama menggunakan `readonly`, sehingga tidak dapat diubah setelah diinisialisasi. Atribut nilai tugas, UTS, dan UAS tidak menggunakan `readonly`.

3) **Constructor**

   Constructor menggunakan fitur constructor property promotion PHP untuk mendeklarasikan dan mengisi atribut. NIM diperiksa menggunakan `trim()` agar NIM yang kosong atau hanya berisi spasi ditolak.

4) **Method `pastikanNilaiSah()`**

   Method privat ini memeriksa apakah nilai berada dalam rentang 0–100. Jika tidak sesuai, program menghasilkan `InvalidArgumentException`.

5) **Method `nilaiAkhir()`**

   Method ini menghitung nilai akhir berdasarkan bobot tugas 30%, UTS 30%, dan UAS 40%.

6) **Method `hurufMutu()`**

   Method ini menentukan huruf mutu menggunakan `match` berdasarkan nilai akhir mahasiswa.

7) **Getter**

   Method `getNim()` dan `getNama()` digunakan untuk mengambil NIM dan nama mahasiswa.

8) **Method `__toString()`**

   Method ini mengatur format tampilan data mahasiswa agar dapat ditampilkan dengan rapi.

### b. main.php

File `main.php` digunakan untuk menjalankan dan menguji class `Mahasiswa` pada PHP.

1) Program memanggil file `Mahasiswa.php` menggunakan `require_once`.

2) Program membuat tiga objek mahasiswa dengan data yang sama seperti pengujian Java.

3) Perulangan `foreach` digunakan untuk menampilkan data mahasiswa.

4) Program menguji nilai tugas 150. Data tersebut akan ditolak karena berada di luar rentang nilai yang diperbolehkan.

5) Program menguji NIM kosong. Jika terjadi kesalahan validasi, program menangkap `InvalidArgumentException` dan menampilkan pesan penolakan.

## 4. Hasil Pengujian

### A. Sebelum Perbaikan

**Output Java**

Masukkan screenshot output Java sebelum perbaikan di sini.

**Output PHP**

Masukkan screenshot output PHP sebelum perbaikan di sini.

### B. Sesudah Perbaikan

**Output Java**

Masukkan screenshot output Java sesudah perbaikan di sini.

**Output PHP**

Masukkan screenshot output PHP sesudah perbaikan di sini.

## 5. Kesimpulan

Pada praktikum Pertemuan 2, enkapsulasi digunakan untuk melindungi data mahasiswa dan menjaga agar data tetap sesuai dengan aturan yang ditentukan. Penggunaan atribut `private`, `final`, dan `readonly`, serta validasi pada constructor membantu mencegah data yang tidak valid. Program juga dapat menghitung nilai akhir, menentukan huruf mutu, dan menolak NIM kosong maupun nilai di luar rentang 0–100. Implementasi Java dan PHP memiliki fungsi yang sama dengan sintaks yang berbeda.
