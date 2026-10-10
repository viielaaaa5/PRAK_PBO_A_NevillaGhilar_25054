# Laporan Praktikum 04: Inheritance 

| Keterangan | Detail |
|---|---|
| Nama | Nevilla Ghilar Apryanti |
| NPM | 4525210054 |
| Kelas | PBO A 2025/2026 |
| Mata Kuliah | Pemrograman Berorientasi Objek |
| Dosen Pengampu | Adi Wahyu Pribadi, S.Si., M.Kom. |

## 1. Ringkasan Soal

Praktikum 4 membahas penerapan konsep inheritance (pewarisan) dalam pemrograman berorientasi objek menggunakan Java dan PHP.

Program yang dibuat digunakan untuk mengelola data pegawai dan menghitung gaji berdasarkan jenis pegawai. Class induk `Pegawai` digunakan sebagai dasar, sedangkan class turunannya seperti `PegawaiTetap` dan `PegawaiKontrak` memiliki aturan perhitungan gaji masing-masing.

Tujuan praktikum ini adalah memahami cara menggunakan pewarisan, mengatur atribut dan method dalam class, serta menerapkan perhitungan gaji sesuai ketentuan program.

## 2. Implementasi Java

### A. Kode Sebelum Perbaikan

Pada kode Java sebelum perbaikan, program sudah memiliki struktur untuk mengelola data pegawai, tetapi perhitungan gaji belum berjalan sesuai ketentuan. Akibatnya, gaji pegawai masih menghasilkan nilai Rp0.

**Kode sebelum perbaikan Java:**

[.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan4/Pewarisan/java)

### B. Kode Setelah Perbaikan

Pada kode Java setelah perbaikan, class `Pegawai` digunakan sebagai class induk, kemudian `PegawaiTetap` dan `PegawaiKontrak` menjadi class turunannya. Setiap jenis pegawai dapat memiliki perhitungan gaji yang berbeda sesuai aturan yang diterapkan.

Perbaikan yang dilakukan meliputi:
- Mengatur hubungan pewarisan antara class pegawai.
- Memperbaiki method perhitungan gaji.
- Menggunakan method pada class turunan sesuai jenis pegawai.
- Menampilkan data pegawai dan hasil perhitungan gaji.
- Menghitung total gaji seluruh pegawai.

Berdasarkan hasil eksekusi, gaji Ani berhasil ditampilkan sebesar Rp7.800.000 dengan total gaji Rp12.800.000.

**Kode setelah perbaikan Java:**

[.java](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan4/src)

## 3. Implementasi PHP

### A. Kode Sebelum Perbaikan

Pada implementasi PHP sebelum perbaikan, program digunakan untuk mengelola data pegawai dan menampilkan hasil perhitungan gaji. Namun, perhitungan gaji belum berjalan dengan benar sehingga gaji pegawai masih menghasilkan nilai Rp0.

**Kode sebelum perbaikan PHP:**

[.php](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/Materi%26Code%20Sebelumnya/pertemuan4/Pewarisan/php)

### B. Kode Setelah Perbaikan

Pada kode PHP setelah perbaikan, konsep inheritance diterapkan untuk menghubungkan class induk dengan class turunannya. Program kemudian digunakan untuk menampilkan data pegawai dan menghitung gaji sesuai jenis pegawai.

Perbaikan yang dilakukan meliputi:
- Memperbaiki struktur class dan hubungan pewarisan.
- Menyesuaikan method perhitungan gaji.
- Menampilkan informasi setiap pegawai.
- Menghitung total gaji dari seluruh pegawai yang dibuat.

Berdasarkan hasil eksekusi, program PHP berhasil menampilkan data empat pegawai dengan total gaji sebesar Rp26.440.000.

**Kode setelah perbaikan PHP:**
[.php](https://github.com/viielaaaa5/PRAK_PBO_A_NevillaGhilar_25054/tree/main/PRAK%20PBO/pertemuan4/src)

## 4. Bukti Eksekusi

### A. Eksekusi Java

**Sebelum perbaikan**

<img width="379" height="131" alt="Pertemuan4" src="https://github.com/user-attachments/assets/824e740c-7080-4696-a6d1-438982825a52" />


**Sesudah perbaikan**

<img width="555" height="191" alt="Pertemuan4" src="https://github.com/user-attachments/assets/60b88366-5ada-4c80-93d5-200e4bb1d0ba" />


### B. Eksekusi PHP

**Sebelum perbaikan**

<img width="449" height="163" alt="Pertemuan4" src="https://github.com/user-attachments/assets/7cdd6c27-6a74-405e-9e88-ff455c8ac1b2" />


**Sesudah perbaikan**

<img width="459" height="152" alt="Pertemuan4" src="https://github.com/user-attachments/assets/c4d94c9b-cbdf-4da7-a3c3-381bf630d73e" />


## 5. Kesimpulan

Berdasarkan praktikum yang telah dilakukan, konsep inheritance dapat digunakan untuk membuat hubungan antara class induk dan class turunan. Dengan konsep ini, setiap jenis pegawai dapat memiliki method perhitungan gaji sesuai ketentuannya.

Melalui praktikum ini, saya memahami penerapan inheritance dalam Java dan PHP, serta cara memperbaiki perhitungan gaji dan menampilkan total gaji pegawai melalui program.
