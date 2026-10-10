# Laporan Praktikum PBO A — Pertemuan 4

**Nama:** Nevilla Ghilar Apryanti  
**NPM:** 4525210054

## 1. Deskripsi Tugas

Pada Pertemuan 4, praktikum membahas konsep pewarisan (*inheritance*), class abstract, dan polimorfisme (*polymorphism*). Program digunakan untuk mengelola beberapa jenis pegawai, yaitu pegawai tetap, pegawai kontrak, dosen, dan pegawai harian. Setiap jenis pegawai memiliki aturan perhitungan gaji yang berbeda.

## 2. Penjelasan Kode Java

### a. Pegawai.java

File `Pegawai.java` merupakan class induk atau superclass bagi jenis pegawai lainnya.

1) **Atribut**

   Atribut `nip`, `nama`, dan `gajiPokok` menggunakan `protected final` agar dapat digunakan oleh class turunan dan tidak dapat diubah setelah diinisialisasi.

2) **Constructor**

   Constructor digunakan untuk mengisi data NIP, nama, dan gaji pokok. Program menolak gaji pokok negatif dengan `IllegalArgumentException`.

3) **Method `hitungGaji()`**

   Method ini mengembalikan gaji pokok sebagai perhitungan dasar sebelum ditambahkan tunjangan oleh class turunan.

4) **Method abstract `jenis()`**

   Method ini mewajibkan setiap class turunan menentukan jenis pegawainya sendiri.

5) **Getter**

   Method `getNama()` dan `getNip()` digunakan untuk mengambil nama dan NIP pegawai.

6) **Method `toString()`**

   Method ini mengatur tampilan NIP, jenis pegawai, nama, dan hasil perhitungan gaji.

### b. PegawaiTetap.java

File `PegawaiTetap.java` merupakan class turunan dari `Pegawai` yang digunakan untuk pegawai tetap.

1) **Konstanta tunjangan**

   `TUNJANGAN_PER_TAHUN` menetapkan tunjangan sebesar 2% per tahun, sedangkan `TUNJANGAN_MAKSIMUM` membatasi tunjangan maksimal sebesar 40%.

2) **Atribut `masaKerjaTahun`**

   Atribut ini menyimpan lama masa kerja pegawai dalam tahun.

3) **Constructor**

   Constructor menggunakan `super()` untuk memanggil constructor class induk dan mengisi data pegawai.

4) **Method `hitungGaji()`**

   Method ini menghitung gaji pokok ditambah tunjangan masa kerja. Persentase tunjangan dihitung dari masa kerja dan dibatasi maksimal 40%.

5) **Method `jenis()`**

   Method ini mengembalikan teks `"TETAP"` sebagai jenis pegawai.

6) **Method `getMasaKerjaTahun()`**

   Method ini digunakan untuk mengambil data masa kerja pegawai.

### c. PegawaiKontrak.java

File `PegawaiKontrak.java` merupakan class turunan dari `Pegawai` yang digunakan untuk pegawai kontrak.

1) **Atribut `bulanKontrak`**

   Atribut ini menyimpan lama kontrak kerja dalam bulan.

2) **Constructor**

   Constructor menerima NIP, nama, gaji pokok, dan lama kontrak. Data umum diteruskan ke constructor induk menggunakan `super()`.

3) **Method `jenis()`**

   Method ini mengembalikan teks `"KONTRAK"` sebagai jenis pegawai.

4) **Method `getBulanKontrak()`**

   Method ini digunakan untuk mengambil lama kontrak pegawai.

5) **Perhitungan gaji**

   Class ini tidak perlu melakukan override pada `hitungGaji()` karena pegawai kontrak menggunakan gaji pokok tanpa tambahan tunjangan masa kerja.

### d. Main.java

File `Main.java` digunakan untuk menjalankan program dan menguji perhitungan g
