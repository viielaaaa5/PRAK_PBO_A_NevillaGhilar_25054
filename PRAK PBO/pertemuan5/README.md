# Laporan Praktikum PBO A — Pertemuan 5

**Nama:** Nevilla Ghilar Apryanti  
**NPM:** 4525210054

## 1. Deskripsi Tugas

Pada Pertemuan 5, praktikum membahas konsep polimorfisme (*polymorphism*) menggunakan class abstract dan method abstract. Program membuat beberapa jenis bangun datar, seperti lingkaran, persegi, segitiga, dan trapesium. Setiap bangun datar memiliki cara perhitungan luas dan keliling masing-masing.

Praktikum juga membahas perbedaan antara kode yang menggunakan pemeriksaan tipe (*anti-pattern*) dan kode yang menggunakan polimorfisme.

## 2. Penjelasan Kode Java

### a. BangunDatar.java

File `BangunDatar.java` merupakan class induk abstract untuk semua jenis bangun datar.

1) Atribut `nama` digunakan untuk menyimpan nama bangun datar dan bersifat `private final`.

2) Constructor `BangunDatar()` digunakan untuk mengisi nama bangun datar.

3) Method abstract `luas()` dan `keliling()` menjadi aturan yang harus diimplementasikan oleh setiap class turunan.

4) Method `getNama()` digunakan untuk mengambil nama bangun datar.

5) Method `toString()` mengatur tampilan nama, luas, dan keliling. Method ini memanggil implementasi `luas()` dan `keliling()` dari objek turunannya.

### b. Lingkaran.java

File `Lingkaran.java` berisi class lingkaran yang merupakan turunan dari `BangunDatar`.

1) Atribut `jariJari` menyimpan panjang jari-jari lingkaran.

2) Constructor memanggil `super("Lingkaran")` dan menolak jari-jari yang kurang dari atau sama dengan nol.

3) Method `luas()` menghitung luas menggunakan rumus \(\pi r^2\) dengan `Math.PI`.

4) Method `keliling()` menghitung keliling menggunakan rumus \(2\pi r\).

5) Method `getJariJari()` digunakan untuk mengambil nilai jari-jari.

### c. Persegi.java

File `Persegi.java` berisi class persegi yang merupakan turunan dari `BangunDatar`.

1) Atribut `sisi` menyimpan panjang sisi persegi.

2) Constructor menetapkan nama bangun menjadi `"Persegi"` dan menolak panjang sisi yang kurang dari atau sama dengan nol.

3) Method `luas()` menghitung luas dengan rumus sisi dikali sisi.

4) Method `keliling()` menghitung keliling dengan rumus empat kali panjang sisi.

5) Method `getSisi()` digunakan untuk mengambil panjang sisi persegi.

### d. Segitiga.java

File `Segitiga.java` berisi class segitiga yang merupakan turunan dari `BangunDatar`.

1) Atribut `alas`, `tinggi`, dan `sisiMiring` menyimpan data ukuran segitiga.

2) Constructor menetapkan nama bangun menjadi `"Segitiga"` dan mengisi ketiga atribut tersebut.

3) Method `luas()` menghitung luas menggunakan rumus setengah dikali alas dikali tinggi.

4) Method `keliling()` menghitung keliling dengan menjumlahkan ketiga atribut yang digunakan sebagai sisi.

5) Method `toString()` mengatur tampilan ukuran segitiga dan hasil luasnya.

### e. Trapesium.java

File `Trapesium.java` berisi class trapesium yang merupakan turunan dari `BangunDatar`.

1) Atribut `sisiAtas`, `sisiBawah`, `tinggi`, `sisiKiri`, dan `sisiKanan` menyimpan ukuran trapesium.

2) Constructor mengisi seluruh atribut dan menetapkan nama bangun menjadi `"Trapesium"`.

3) Method `luas()` menghitung luas menggunakan rumus setengah dikali jumlah dua sisi sejajar dikali tinggi.

4) Method `keliling()` menghitung keliling dengan menjumlahkan keempat sisi.

5) Method `toString()` menampilkan ukuran trapesium dan hasil perhitungan luasnya.

### f. Main.java

File `Main.java` digunakan untuk menjalankan program dan menguji perhitungan bangun datar.

1) Program membuat array `BangunDatar[]` yang berisi objek `Lingkaran`, `Persegi`, `Segitiga`, dan `Trapesium`.

2) Perulangan `for` digunakan untuk menampilkan informasi setiap bangun datar.

3) Variabel `total` digunakan untuk menjumlahkan luas seluruh bangun datar melalui method `luas()`.

4) Program menampilkan total luas dengan `System.out.printf()`.

5) Program menampilkan contoh nilai luas lingkaran, persegi, dan segitiga sebagai pemeriksaan hasil perhitungan.

6) Program menggunakan `instanceof` untuk memeriksa objek yang merupakan `Lingkaran`, kemudian menampilkan jari-jarinya melalui `getJariJari()`.

### g. AntiPattern.java

File `AntiPattern.java` menunjukkan contoh kode yang belum menggunakan polimorfisme secara langsung untuk menghitung luas bangun datar.

1) Record `LingkaranData`, `PersegiData`, dan `SegitigaData` digunakan untuk menyimpan data masing-masing bangun.

2) Method `hitungLuas()` menggunakan `instanceof` dan rangkaian `if-else` untuk menentukan rumus luas berdasarkan jenis objek.

3) Method `main()` membuat daftar bangun datar, menghitung luas setiap objek, lalu menampilkan total luas.

4) Pendekatan ini kurang fleksibel karena setiap jenis bangun baru mengharuskan method `hitungLuas()` diubah.

### h. AntiPatternRefaktor.java

File `AntiPatternRefaktor.java` merupakan hasil refaktor dari contoh anti-pattern agar perhitungan luas menggunakan polimorfisme.

1) Interface `Bangun` menetapkan method `luas()` yang harus dimiliki setiap implementasi.

2) Record `LingkaranData` menghitung luas lingkaran menggunakan \(\pi r^2\).

3) Record `PersegiData` menghitung luas persegi menggunakan sisi dikali sisi.

4) Record `SegitigaData` menghitung luas segitiga menggunakan setengah dikali alas dikali tinggi.

5) Array `Bangun[]` menyimpan berbagai jenis objek yang menerapkan interface `Bangun`.

6) Perulangan memanggil method `luas()` dari setiap objek tanpa menggunakan pemeriksaan tipe pada proses perhitungan.

7) Program menampilkan total luas menggunakan pendekatan polimorfisme yang lebih mudah dikembangkan.

## 3. Penjelasan Kode PHP

### a. BangunDatar.php

File `BangunDatar.php` berisi class abstract `BangunDatar` beserta beberapa class turunannya.

1) **Class `BangunDatar`**

   Menyimpan nama bangun datar dan menetapkan method abstract `luas()` serta `keliling()` yang wajib diimplementasikan oleh class turunan.

2) **Class `Lingkaran`**

   Menyimpan jari-jari, memvalidasi agar jari-jari lebih besar dari nol, menghitung luas menggunakan `M_PI`, dan menghitung keliling lingkaran.

3) **Class `Persegi`**

   Menyimpan panjang sisi, memvalidasi sisi, serta menghitung luas dan keliling persegi.

4) **Class `Segitiga`**

   Menyimpan tiga sisi, memvalidasi agar semua sisi positif dan memenuhi syarat pembentukan segitiga. Luas dihitung menggunakan rumus Heron, sedangkan keliling diperoleh dari jumlah ketiga sisi.

5) **Class `Trapesium`**

   Menyimpan dua sisi sejajar, dua sisi miring, dan tinggi. Luas dihitung dari setengah jumlah sisi sejajar dikali tinggi, sedangkan keliling dihitung dari jumlah keempat sisinya.

6) **Method `__toString()`**

   Method pada class induk mengatur tampilan nama, luas, dan keliling setiap bangun datar.

7) **Driver code**

   Bagian akhir file membuat objek lingkaran, persegi, segitiga, dan trapesium, kemudian menampilkan hasil perhitungannya.

### b. main.php

File `main.php` digunakan untuk menjalankan program perhitungan bangun datar menggunakan PHP.

1) Program memanggil `BangunDatar.php` menggunakan `require_once`.

2) Variabel `$daftar` berisi objek `Lingkaran(7)`, `Persegi(5)`, dan `Segitiga(3, 4, 5)`.

3) Perulangan `foreach` digunakan untuk menampilkan setiap objek bangun datar.

4) Fungsi `array_map()` memanggil method `luas()` dari setiap objek, kemudian `array_sum()` menjumlahkan seluruh hasilnya.

5) Program menampilkan total luas menggunakan `printf()` dengan dua angka di belakang koma.

6) Program menampilkan nilai luas yang diharapkan untuk lingkaran, persegi, dan segitiga sebagai pemeriksaan hasil perhitungan.

### c. Notifikasi.php

File `Notifikasi.php` berisi contoh latihan mandiri mengenai polimorfisme menggunakan sistem notifikasi.

1) **Class abstract `Notifikasi`**

   Menyimpan tujuan notifikasi dan menetapkan method abstract `kirim()` serta `saluran()`.

2) **Class `Email`**

   Mengirim pesan dalam format email dengan tujuan berupa alamat email.

3) **Class `SMS`**

   Menampilkan pesan SMS dengan tujuan berupa nomor telepon.

4) **Class `WhatsApp`**

   Menampilkan pesan WhatsApp dengan tujuan berupa nomor telepon.

5) **Function `kirimSemua()`**

   Mengirim pesan ke seluruh objek notifikasi menggunakan perulangan dan method `kirim()`, tanpa perlu memeriksa jenis objek menggunakan `instanceof`, `match`, atau `switch`.

6) **Pengujian notifikasi**

   Program membuat objek Email, SMS, dan WhatsApp, kemudian mengirimkan pesan yang sama melalui ketiga saluran tersebut.

## 4. Hasil Pengujian

### A. Sebelum Perbaikan

**Output Java**

Masukkan screenshot hasil output Java sebelum perbaikan di sini.

**Output PHP**

Masukkan screenshot hasil output PHP sebelum perbaikan di sini.

### B. Sesudah Perbaikan

**Output Java**

Masukkan screenshot hasil output Java sesudah perbaikan di sini.

**Output PHP**

Masukkan screenshot hasil output PHP sesudah perbaikan di sini.

## 5. Kesimpulan

Pada praktikum Pertemuan 5, polimorfisme digunakan agar berbagai objek dapat diproses melalui method yang sama dengan implementasi berbeda. Class abstract dan interface menetapkan kontrak yang harus dipenuhi oleh class turunannya. Program bangun datar dapat menghitung luas dan keliling sesuai jenis objek, sedangkan contoh notifikasi menunjukkan bahwa pesan dapat dikirim melalui berbagai saluran tanpa pemeriksaan tipe. Refaktor dari anti-pattern juga membuat program lebih mudah dikembangkan ketika jenis objek baru ditambahkan.
