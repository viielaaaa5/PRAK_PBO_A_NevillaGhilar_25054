# Laporan Praktikum 06: Interface, Abstract Class, dan Enum

| Keterangan | Detail |
|---|---|
| Nama | Nevilla Ghilar Apryanti |
| NPM | 4525210054 |
| Kelas | PBO A 2025/2026 |
| Mata Kuliah | Pemrograman Berorientasi Objek |
| Dosen Pengampu | Adi Wahyu Pribadi, S.Si., M.Kom. |

## 1. Ringkasan Soal

Praktikum 6 membahas penerapan konsep interface, abstract class, enum, dan trait dalam pemrograman berorientasi objek menggunakan Java dan PHP.

Program yang dibuat digunakan untuk menggambarkan kendaraan, seperti mobil dan sepeda. Setiap kendaraan memiliki karakteristik dan kemampuan yang berbeda, seperti jumlah roda, kecepatan maksimum, dan cara bergerak.

Program juga menerapkan interface `Movable` untuk kendaraan yang dapat bergerak, interface `Fuelable` untuk kendaraan yang dapat diisi bahan bakar, serta enum `TipeBahanBakar` untuk menentukan jenis bahan bakar dan biayanya.

## 2. Implementasi Java

### A. Kode Sebelum Perbaikan

Pada kode Java sebelum perbaikan, program digunakan sebagai dasar untuk mengimplementasikan kendaraan dan kemampuan yang dimilikinya. Struktur program perlu disesuaikan agar kendaraan dapat memiliki perilaku yang berbeda berdasarkan jenis dan kemampuannya.

**Kode sebelum perbaikan Java:**

[.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan6/06-abstract-class-interface-enum-dan-trait/starter/java)

### B. Kode Setelah Perbaikan

Pada kode Java setelah perbaikan, program menerapkan beberapa konsep pemrograman berorientasi objek.

Perbaikan yang dilakukan meliputi:

- Membuat abstract class `Kendaraan` sebagai dasar untuk objek kendaraan.
- Menggunakan interface `Movable` untuk mengatur kemampuan kendaraan bergerak.
- Menggunakan interface `Fuelable` untuk kendaraan yang dapat diisi bahan bakar.
- Menggunakan enum `TipeBahanBakar` untuk menentukan jenis bahan bakar, biaya pengisian, dan sifat ramah lingkungan.
- Mengimplementasikan class `Mobil` dan `Sepeda` dengan karakteristik masing-masing.
- Membuat program utama untuk menampilkan informasi kendaraan dan menghitung biaya pengisian bahan bakar.

Pada hasil program, mobil Toyota Avanza dapat bergerak dan diisi bahan bakar sesuai kapasitas tangkinya, sedangkan sepeda Polygon hanya memiliki kemampuan bergerak dan tidak dapat diisi bahan bakar.

**Kode setelah perbaikan Java:**

[.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan6/src/java)

## 3. Implementasi PHP

### A. Kode Sebelum Perbaikan

Pada kode PHP sebelum perbaikan, program digunakan sebagai dasar untuk mengelola objek kendaraan. Implementasi kemudian disesuaikan agar dapat menerapkan interface, abstract class, enum, dan trait sesuai kebutuhan program.

**Kode sebelum perbaikan PHP:**

[.php](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan6/06-abstract-class-interface-enum-dan-trait/starter/php)

### B. Kode Setelah Perbaikan

Pada kode PHP setelah perbaikan, program menggunakan abstract class `Kendaraan` sebagai dasar untuk class mobil dan sepeda. Interface `Movable` dan `Fuelable` digunakan untuk membedakan kemampuan setiap kendaraan.

Perbaikan yang dilakukan meliputi:

- Menggunakan abstract class untuk menyimpan atribut dan perilaku umum kendaraan.
- Menerapkan interface `Movable` dan `Fuelable`.
- Menggunakan enum `TipeBahanBakar` untuk menentukan jenis dan biaya bahan bakar.
- Menggunakan trait `Loggable` untuk mencatat informasi objek.
- Membuat class `Mobil`, `Sepeda`, dan `Pesanan` sesuai fungsinya.
- Menampilkan informasi kendaraan, biaya pengisian bahan bakar, serta contoh penggunaan trait.

Pada hasil program, mobil dapat diisi bahan bakar hingga kapasitas tangki, sedangkan sepeda tidak dapat diberikan ke fungsi pengisian bahan bakar karena tidak mengimplementasikan interface `Fuelable`.

**Kode setelah perbaikan PHP:**

[.php](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan6/src/php)

## 4. Bukti Eksekusi

### A. Eksekusi Java

**Sebelum perbaikan**

<img width="383" height="153" alt="Pertemuan6" src="https://github.com/user-attachments/assets/474a52fe-4341-43a3-aaa5-b2468a3ab881" />


**Sesudah perbaikan**

<img width="370" height="141" alt="Pertemuan6" src="https://github.com/user-attachments/assets/64b9cd1e-2409-48a1-bfe9-7596f76b0bef" />


### B. Eksekusi PHP

**Sebelum perbaikan**

<img width="395" height="189" alt="Pertemuan6" src="https://github.com/user-attachments/assets/099743f5-c186-46c9-9204-0c2f441c7a0a" />


**Sesudah perbaikan**

<img width="538" height="212" alt="Pertemuan6" src="https://github.com/user-attachments/assets/7cdd863a-8f8b-4587-aa01-5a16554c4516" />


## 5. Kesimpulan

Berdasarkan praktikum yang telah dilakukan, interface digunakan untuk menentukan kemampuan yang harus dimiliki suatu class, sedangkan abstract class digunakan sebagai dasar untuk class turunannya. Enum membantu mengelompokkan pilihan jenis bahan bakar, dan trait pada PHP dapat digunakan kembali oleh beberapa class.

Melalui praktikum ini, saya memahami cara menerapkan interface, abstract class, enum, dan trait dalam Java dan PHP untuk membuat program kendaraan yang lebih terstruktur sesuai kemampuan masing-masing objek.
