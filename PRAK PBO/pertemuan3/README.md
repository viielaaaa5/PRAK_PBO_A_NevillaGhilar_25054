# Laporan Praktikum PBO A — Pertemuan 3

**Nama:** Nevilla Ghilar Apryanti  
**NPM:** 4525210054

## 1. Deskripsi Tugas

Pada Pertemuan 3, praktikum membahas constructor berdelegasi, anggota statis (*static*), konstanta, dan enkapsulasi pada class `RekeningBank`. Program digunakan untuk mengelola rekening bank, seperti membuat rekening, melakukan setoran dan penarikan, memotong biaya administrasi, menghitung jumlah rekening, serta menghitung bunga tahunan.

Program juga menerapkan validasi untuk menjaga saldo agar tidak negatif dan memastikan transaksi sesuai dengan aturan yang ditentukan.

## 2. Penjelasan Kode Java

### a. RekeningBank.java

File `RekeningBank.java` berisi class `RekeningBank` yang digunakan untuk mengelola data dan operasi rekening bank.

1) **Konstanta**

   `bunga_tahunan`, `biaya_administrasi`, dan `batas_penarikan_sekali` digunakan untuk menyimpan nilai bunga tahunan, biaya administrasi, dan batas maksimal penarikan dalam satu transaksi.

2) **Atribut rekening**

   Atribut `nomor` dan `pemilik` menggunakan `private final` agar tidak dapat diubah setelah objek dibuat. Atribut `saldo` dapat berubah sesuai transaksi yang dilakukan.

3) **Atribut static `jumlahRekening`**

   Atribut ini digunakan untuk menghitung jumlah rekening yang berhasil dibuat. Karena menggunakan `static`, nilainya dimiliki bersama oleh seluruh objek `RekeningBank`.

4) **Constructor ringkas**

   Constructor `RekeningBank(String nomor, String pemilik)` digunakan untuk membuat rekening tanpa menentukan saldo awal. Pada implementasi yang sesuai dengan konsep delegasi, constructor ini memanggil constructor lengkap menggunakan `this(...)`.

5) **Constructor lengkap**

   Constructor ini menerima nomor rekening, nama pemilik, dan saldo awal. Validasi dilakukan untuk menolak nomor rekening kosong dan saldo awal negatif. Setelah rekening berhasil dibuat, jumlah rekening bertambah satu.

6) **Method `setor()`**

   Method ini digunakan untuk menambahkan saldo. Jumlah setoran harus lebih besar dari nol.

7) **Method `tarik()`**

   Method ini digunakan untuk mengurangi saldo. Penarikan ditolak jika jumlahnya tidak positif, melebihi saldo yang tersedia, atau melebihi batas penarikan per transaksi.

8) **Method `potongBiayaAdmin()`**

   Method ini mengurangi saldo sebesar biaya administrasi. Penggunaan `Math.max()` menjaga saldo agar tidak menjadi negatif.

9) **Method `getJumlahRekening()`**

   Method static ini mengembalikan jumlah rekening yang telah berhasil dibuat.

10) **Method `bungaSetahun()`**

    Method static ini menghitung bunga tahunan berdasarkan jumlah saldo pokok dan konstanta bunga tahunan.

11) **Getter**

    Method `getSaldo()` digunakan untuk mengambil saldo rekening, sedangkan `getNomor()` digunakan untuk mengambil nomor rekening.

12) **Method `toString()`**

    Method ini mengatur format tampilan nomor rekening, nama pemilik, dan saldo agar hasilnya lebih rapi.

### b. Main.java

File `Main.java` digunakan untuk menjalankan dan menguji class `RekeningBank`.

1) Program menampilkan jumlah rekening pada awal program melalui `getJumlahRekening()`.

2) Program membuat tiga objek rekening milik Ani, Budi, dan Citra. Rekening Budi dibuat menggunakan constructor ringkas.

3) Program menampilkan informasi ketiga rekening menggunakan `System.out.println()`.

4) Program menampilkan jumlah rekening setelah objek dibuat untuk memastikan penghitung rekening menunjukkan angka tiga.

5) Program melakukan setoran sebesar Rp500.000 ke rekening Ani, kemudian menampilkan saldo setelah setoran.

6) Program mencoba melakukan penarikan sebesar Rp9.999.999. Karena penarikan melanggar aturan, program menangkap kesalahan dan menampilkan pesan penolakan.

7) Program memotong biaya administrasi rekening Budi dan menampilkan saldonya untuk memastikan saldo tidak negatif.

8) Program menghitung bunga setahun dari saldo Ani menggunakan method static `bungaSetahun()`.

## 3. Penjelasan Kode PHP

### a. RekeningBank.php

File `RekeningBank.php` merupakan implementasi class rekening bank menggunakan PHP dengan fungsi yang setara dengan versi Java.

1) **Konstanta**

   Konstanta `BUNGA_TAHUNAN`, `BIAYA_ADMINISTRASI`, dan `BATAS_PENARIKAN_SEKALI` digunakan untuk menyimpan nilai bunga, biaya administrasi, dan batas penarikan.

2) **Atribut static `jumlahRekening`**

   Atribut ini digunakan untuk menghitung jumlah rekening yang berhasil dibuat dan dimiliki bersama oleh seluruh objek.

3) **Atribut rekening**

   Atribut `nomor` dan `pemilik` menggunakan `readonly` agar tidak dapat diubah setelah diinisialisasi. Atribut `saldo` digunakan untuk menyimpan saldo rekening.

4) **Constructor**

   Constructor menerima nomor rekening, nama pemilik, dan saldo awal. Parameter saldo awal memiliki nilai default nol. Constructor juga memvalidasi nomor rekening dan saldo awal sebelum menambah jumlah rekening.

5) **Method `rekeningPelajar()`**

   Method static ini merupakan *named constructor* yang digunakan untuk membuat rekening pelajar dengan saldo awal nol.

6) **Method `setor()`**

   Method ini menambahkan saldo rekening jika jumlah setoran lebih besar dari nol.

7) **Method `tarik()`**

   Method ini memvalidasi jumlah penarikan, kecukupan saldo, dan batas maksimal penarikan per transaksi sebelum mengurangi saldo.

8) **Method `potongBiayaAdmin()`**

   Method ini mengurangi saldo sebesar biaya administrasi menggunakan `max()` agar saldo tidak negatif.

9) **Method `getJumlahRekening()`**

   Method static ini mengembalikan jumlah rekening yang telah berhasil dibuat.

10) **Method `bungaSetahun()`**

    Method ini menghitung bunga tahunan berdasarkan saldo pokok dan konstanta bunga.

11) **Getter**

    Method `getSaldo()` dan `getNomor()` digunakan untuk mengambil saldo dan nomor rekening.

12) **Method `__toString()`**

    Method ini mengatur tampilan informasi rekening dan memformat saldo menggunakan `number_format()`.

### b. main.php

File `main.php` digunakan untuk menjalankan dan menguji class `RekeningBank` pada PHP.

1) Program memanggil file `RekeningBank.php` menggunakan `require_once`.

2) Program menampilkan jumlah rekening awal, kemudian membuat rekening Ani, Budi, dan Citra.

3) Rekening Ani dan Citra dibuat menggunakan constructor biasa, sedangkan rekening Budi dibuat menggunakan method `rekeningPelajar()`.

4) Program menampilkan informasi ketiga rekening dan jumlah rekening setelah objek dibuat.

5) Program melakukan setoran Rp500.000 ke rekening Ani dan menampilkan saldo setelah transaksi.

6) Program mencoba melakukan penarikan Rp9.999.999. Jika transaksi ditolak, program menangkap exception dan menampilkan pesan kesalahan.

7) Program memotong biaya administrasi rekening Budi dan menampilkan saldo setelah pemotongan.

8) Program menghitung bunga tahunan dari saldo Ani dan menampilkan hasilnya dalam format rupiah.

## 4. Hasil Pengujian

### A. Sebelum Perbaikan

**Output Java**
<img width="422" height="179" alt="Pertemuan3" src="https://github.com/user-attachments/assets/772b9053-6276-485c-be5a-6b53197d7ffb" />



**Output PHP**

<img width="472" height="190" alt="Pertemuan3" src="https://github.com/user-attachments/assets/85a58256-9c53-403d-b3e9-827b4654d656" />



### B. Sesudah Perbaikan

**Output Java**

<img width="536" height="179" alt="Pertemuan3" src="https://github.com/user-attachments/assets/b509cfde-bd52-4cda-8124-700eebd4e438" />


**Output PHP**

<img width="535" height="171" alt="Pertemuan3" src="https://github.com/user-attachments/assets/548cf791-efa2-422f-be56-ccae486619e1" />


## 5. Kesimpulan

Pada praktikum Pertemuan 3, program rekening bank menerapkan constructor, konstanta, atribut dan method static, serta enkapsulasi. Constructor digunakan untuk membuat objek rekening, sedangkan validasi menjaga agar data dan transaksi sesuai aturan. Atribut static digunakan untuk menghitung jumlah rekening, dan method static digunakan untuk menghitung bunga tahunan. Dengan penerapan tersebut, program dapat mengelola rekening serta mencegah transaksi yang tidak valid.
