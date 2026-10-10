# Panduan Laporan Sebelum & Sesudah — PBO A (Nevilla Ghilar Apryanti, 4525210054)

## 1. Pertemuan 6 — Interface, Abstract Class, Enum, dan Trait

Praktikum ini membahas penggunaan interface, abstract class, enum, dan trait pada Java dan PHP. Program yang dibuat membahas kendaraan, kemampuan bergerak, pengisian bahan bakar, dan penggunaan kembali method.

## 2. Penjelasan File Java

### 1) `Fuelable.java`

File ini berisi interface `Fuelable` sebagai kontrak untuk objek yang dapat diisi bahan bakar. Method yang tersedia yaitu `isiBahanBakar()`, `kapasitasTangki()`, dan `tipeBahanBakar()`.

### 2) `Kendaraan.java`

File ini merupakan abstract class yang menjadi induk kendaraan. Class ini memiliki atribut merek dan tahun, method `umur()` untuk menghitung umur kendaraan, serta method abstrak `jumlahRoda()`.

### 3) `Main.java`

File ini merupakan program utama untuk menjalankan objek mobil dan sepeda. Program menampilkan kendaraan yang bisa bergerak, mengisi bahan bakar mobil hingga penuh, serta menampilkan informasi jenis dan biaya bahan bakar.

### 4) `Mobil.java`

File ini merupakan turunan dari `Kendaraan` yang mengimplementasikan interface `Movable` dan `Fuelable`. Class ini mengatur pergerakan mobil, kecepatan maksimum, kapasitas tangki, dan proses pengisian bahan bakar.

### 5) `Movable.java`

File ini berisi interface yang menentukan kemampuan suatu objek untuk bergerak. Di dalamnya terdapat method `bergerak()`, `kecepatanMaksimum()`, dan default method `ringkasanGerak()` untuk menampilkan ringkasan kecepatan.

### 6) `Sepeda.java`

File ini merupakan turunan dari `Kendaraan` yang mengimplementasikan interface `Movable`. Sepeda dapat bergerak dan memiliki kecepatan maksimum, tetapi tidak mengimplementasikan `Fuelable` karena tidak membutuhkan bahan bakar.

### 7) `TipeBahanBakar.java`

File ini berisi enum dengan tiga jenis bahan bakar, yaitu BENSIN, SOLAR, dan LISTRIK. Enum ini menyimpan label dan harga per satuan serta memiliki method untuk menghitung biaya pengisian dan menentukan apakah bahan bakar ramah lingkungan.

## 3. Penjelasan File PHP

### 1) `abstraksi.php`

File ini berisi interface `Movable` dan `Fuelable`, enum `TipeBahanBakar`, trait `Loggable`, abstract class `Kendaraan`, serta class `Mobil`, `Sepeda`, dan `Pesanan`.

Interface digunakan untuk menentukan kemampuan suatu objek. Abstract class menjadi dasar bagi class turunannya, enum mengatur jenis bahan bakar, sedangkan trait menyediakan method `log()` yang dapat digunakan oleh class berbeda.

### 2) `main.php`

File ini merupakan program utama PHP yang menjalankan objek mobil dan sepeda. Program menampilkan gerakan kendaraan, kecepatan maksimum, biaya pengisian bahan bakar, serta penggunaan trait `Loggable` pada objek mobil dan pesanan.

## 4. Screenshot Sebelum dan Sesudah

### 1) Sebelum Perbaikan

Masukkan screenshot output program sebelum bagian praktikum diselesaikan atau sebelum perbaikan dilakukan.

### 2) Sesudah Perbaikan

Masukkan screenshot output program setelah bagian praktikum diselesaikan dan program berhasil dijalankan.

Screenshot yang dimasukkan berupa hasil output program sebelum dan sesudah, bukan screenshot kode.

## 5. Kesimpulan

Berdasarkan praktikum pertemuan 6, interface digunakan untuk menentukan kemampuan yang harus dimiliki suatu class, sedangkan abstract class menjadi dasar bagi class turunannya. Enum digunakan untuk mengelola pilihan jenis bahan bakar beserta perilakunya, dan trait pada PHP memungkinkan penggunaan kembali method pada class yang berbeda. Konsep-konsep tersebut membantu membuat program lebih terstruktur dan mudah dikembangkan.
